# Экспресс введение в Symfony и не только ;)

## Введение
Окей, перед собой мы видим замечательный фреймворк Symfony2, который, кроме того что он просто замечательный, является еще и нашим основным рабочим инструментом.

С чего же стоит начать его изучение?

Для начала стоит понять, почему мы выбрали для работы именно Symfony, а не например, Laravel, Yii или, упаси боже, Zend?

+ [http://symfony.com/why-use-a-framework](http://symfony.com/why-use-a-framework)
+ [http://symfony.com/when-use-a-framework](http://symfony.com/when-use-a-framework)
+ [http://symfony.com/ten-criteria](http://symfony.com/ten-criteria)
+ [http://symfony.com/six-good-reasons](http://symfony.com/six-good-reasons)
+ [http://symfony.com/six-technical-reasons](http://symfony.com/six-technical-reasons)

## Начала начал
С этим я думаю становится понятнее, почему мы работаем именно с Symfony и теперь можно перейти непосредственно к изучению самого фреймворка и того, как у него внутри все устроено.

Первым делом установим и настроим Symfony
[http://symfony.com/doc/current/book/installation.html](http://symfony.com/doc/current/book/installation.html), особое внимание уделяем [http://symfony.com/doc/current/book/installation.html#checking-symfony-application-configuration-and-setup](http://symfony.com/doc/current/book/installation.html#checking-symfony-application-configuration-and-setup) этому пункту. Возможно придется немного настроить свой сервер. 
Теперь, когда все настроено, немного поупражняемся в создании страничек
[http://symfony.com/doc/current/book/page_creation.html](http://symfony.com/doc/current/book/page_creation.html)

Какие тут могут возникнуть сложности?

+ Нет прав на запись в директории logs и cache? Выдаем.
+ Не настроено подключение к базе данных? Настраиваем =)

## Дальше самое весёлое
Теперь самое время постараться понять, как же оно все работает.

Начать стоит с медитации на эту статью [http://symfony.com/doc/current/book/http_fundamentals.html](http://symfony.com/doc/current/book/http_fundamentals.html) в ней в общих чертах описывается то как происходит взаимодействие в системе.

Теперь, я надеюсь, у вас есть общее представление о том, что вообще происходит в общих чертах.

Дальше, мы немного сменим ресурс и форму «обучения» на просмотр видео.

+ [https://knpuniversity.com/screencast/symfony2-ep1](https://knpuniversity.com/screencast/symfony2-ep1)
+ [https://knpuniversity.com/screencast/symfony2-ep2](https://knpuniversity.com/screencast/symfony2-ep2)
+ [https://knpuniversity.com/screencast/symfony2-ep3](https://knpuniversity.com/screencast/symfony2-ep3)
+ [https://knpuniversity.com/screencast/symfony2-ep4](https://knpuniversity.com/screencast/symfony2-ep4)

Чем хорошие эти видео? Они рассказывают в общем-то о всех моментах повседневной работы с Symfony. Поэтому смотрим, попутно выполняем все «задания» которые рассматриваются в видео.

Отлично, теперь самое время переходить к чтению документации и расширению тех знаний, которые были получены при просмотре видео.

## Основная документация
+ [http://symfony.com/doc/current/book/controller.html](http://symfony.com/doc/current/book/controller.html) — различные аспекты работы с контроллерами.
+ [http://symfony.com/doc/current/book/routing.html](http://symfony.com/doc/current/book/routing.html) — как создавать правильные пути, на благо себе и ближнему.
+ [http://symfony.com/doc/current/book/doctrine.html](http://symfony.com/doc/current/book/doctrine.html) — информация. Тут самое главное понять, что ORM это не ActiveRecord. В базе, а соответственно и в сущностях, которые мапят базу, у нас хранятся только данные, с самым минимальным набором бизнес логики, которая позволяет поддерживать эти данные. Вся бизнес логика должна находиться в каких-либо сервисах. Дополнительную и полную информацию по работе именно с Doctrine можно посмотреть на официальном сайте Doctrine [http://docs.doctrine-project.org/projects/doctrine-orm/en/latest/](http://docs.doctrine-project.org/projects/doctrine-orm/en/latest/)
+ [http://symfony.com/doc/current/book/templating.html](http://symfony.com/doc/current/book/templating.html) — данные есть, пути есть, контроллеры есть, остался только templating. Для работы с шаблонами Symfony использует twig, у которого так же есть подробная документация на официальном сайте http://twig.sensiolabs.org/documentation

На этом моменте, я очень надеюсь, у вас уже должно сформироваться определенное видение того, как Symfony работает =) Но и это ещё не все. Есть ещё несколько очень важных тем, которые стоит прочитать в документации

+ [http://symfony.com/doc/current/book/forms.html](http://symfony.com/doc/current/book/forms.html) — работа с формами
+ [http://symfony.com/doc/current/book/security.html](http://symfony.com/doc/current/book/security.html) — security
+ [http://symfony.com/doc/current/book/translation.html](http://symfony.com/doc/current/book/translation.html) — переводы
+ [http://symfony.com/doc/current/book/service_container.html](http://symfony.com/doc/current/book/service_container.html) — DI, он же ServiceContainer

Evercode Related
Отлично! У нас уже есть определённый опыт по тому, как мы работаем с Symfony, по этому можно перейти конкретно к тем практикам, которые мы применяем в Evercode Lab.

Первое, стиль написание кода [https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style](https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style)
Второе, в целом имеет раскрывает лучшие практики (best practices) которые приняты у нас к работе. Да, они же приняты как лучшие практики Symfony комьюнити [http://symfony.com/doc/current/best_practices/index.html](http://symfony.com/doc/current/best_practices/index.html)

Для ускорения работы, мы используем свою небольшую сборку Symfony [https://github.com/EvercodeLab/symfony-skeleton](https://github.com/EvercodeLab/symfony-skeleton). В целом это тот же Symfony Standart Edition, просто с уже подключёнными бандлами, которые мы обычно используем в своей работе. Кроме того, там у нас есть набор полезных bash скриптов, которые упрощают развертывание проекта на локальной машине, а так же его обновление в процессе разработки. В данный момент у нас есть версия только для «обычного» стэка. В дальнейшем может появиться собранный набор конкретно для работы с API.

