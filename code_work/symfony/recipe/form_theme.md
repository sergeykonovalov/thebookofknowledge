# Создание и использование кастомных тем для форм в Symfony

Так как формы в Symfony состоят из отдельных компонентов, это позволяет нам довольно легко изменять их под свои нужды и дизайн.

Для начала можно посмотреть на код уже встроенных в Symfony сниппетов для форм: [стандартный div layout](https://github.com/symfony/symfony/blob/master/src/Symfony/Bridge/Twig/Resources/views/Form/form_div_layout.html.twig), [bootstrap 3](https://github.com/symfony/symfony/blob/master/src/Symfony/Bridge/Twig/Resources/views/Form/bootstrap_3_layout.html.twig)

Для примера переопределим `block form_row` из стандартного `form_div_layout`

```twig
{%- block form_row -%}
   <div>
       {{- form_label(form) -}}
       {{- form_errors(form) -}}
       {{- form_widget(form) -}}
   </div>
{%- endblock form_row -%}
```
Добавим к блоку какой-нибудь класс и убираем вывод ошибок (конечно, так делать не стоит, но для примера сойдёт)

```twig
{%- block form_row -%}
    <div class=”some-awesome-class”>
        {{- form_label(form) -}}
        {{- form_widget(form) -}}
    </div>
{%- endblock form_row -%}
```

Теперь осталось только использовать данный кусок кода, что бы изменить отображение формы. Тут у нас есть несколько вариантов.

## Использование снипета прямо в файле с формой
В данном случае у нас будет использоваться основной файл `form_div_layout.html.twig`, но блок `form_row` будет переопределён на наш. Данный способ хорошо только в тех случаях, когда нам надо сделать простую кастомизацию форм, потому что у него есть сложности с использованием переменных формы.

```twig
{%- block form_row -%}
    <div class=”some-awesome-class”>
        {{- form_label(form) -}}
        {{- form_widget(form) -}}
    </div>
{%- endblock form_row -%}

{% form_theme form ‘form_div_layout.html.twig’ _self %}

{% block content %}
    {# ... render the form #}

    {{ form_row(form.age) }}
{% endblock %}
```

## Вынести изменения в отдельный файл, который подключается для каждой формы отдельно
2) Данный способ добавляет нам возможность переиспользования темизации формы только в тех шаблонах, в которых у нас есть необходимость его использовать.

```twig
{# redifned_form_div_layout.html.twig #}

{% extends 'form_div_layout.html.twig' %}

{%- block form_row -%}
    <div class=”some-awesome-class”>
        {{- form_label(form) -}}
        {{- form_widget(form) -}}
    </div>
{%- endblock form_row -%}
```

```twig
{# layout.html.twig #}

{% form_theme form redifned_form_div_layout.html.twig’ %}

{% block content %}
    {# ... render the form #}

    {{ form_row(form.age) }}
{% endblock %}
```

## Тот же файл, но подключаемый глобально для всего приложения

```yaml
# app/config/config.yml
twig:
    form_themes:
        - 'form/fields.html.twig'
```

```twig
{# layout.html.twig #}

{% form_theme form redifned_form_div_layout.html.twig’ %}

{% block content %}
    {# ... render the form #}

    {{ form_row(form.age) }}
{% endblock %}
```

## Официальная документация
* [Forms: Form Theming](http://symfony.com/doc/current/book/forms.html#form-theming)
* [How to Customize Form Rendering](http://symfony.com/doc/current/cookbook/form/form_customization.html)
