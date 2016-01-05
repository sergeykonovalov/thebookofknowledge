# Создание и использование кастомных тем для форм в Symfony

Формы в Symfony состоят из отдельных компонентов, это позволяет изменять их внешний вид под свои нужды.

Посмотрим на код встроенных в Symfony тем для форм: [стандартный div layout](https://github.com/symfony/symfony/blob/master/src/Symfony/Bridge/Twig/Resources/views/Form/form_div_layout.html.twig), [bootstrap 3](https://github.com/symfony/symfony/blob/master/src/Symfony/Bridge/Twig/Resources/views/Form/bootstrap_3_layout.html.twig)

Переопределим `block form_row` из стандартного `form_div_layout`.

```twig
{%- block form_row -%}
   <div>
       {{- form_label(form) -}}
       {{- form_errors(form) -}}
       {{- form_widget(form) -}}
   </div>
{%- endblock form_row -%}
```
Добавим к блоку класс и убирём вывод ошибок.

```twig
{%- block form_row -%}
    <div class=”some-awesome-class”>
        {{- form_label(form) -}}
        {{- form_widget(form) -}}
    </div>
{%- endblock form_row -%}
```

Для использования переопределённого блока есть несколько вариантов.

## Использование сниппета в шаблоне страницы с формой

В этом случае по умолчанию используется `form_div_layout.html.twig`, но блок `form_row` переопределён. Данный способ хорош для простой кастомизации форм.

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

## Создание отдельного файла темы

Этот способ позволяет переиспользовать тему для выбранных форм без копирования блока в каждый шаблон.

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

## Создание отдельного файла темы для всего приложения

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
