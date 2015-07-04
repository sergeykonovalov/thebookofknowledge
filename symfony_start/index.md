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
* [http://symfony.com/doc/current/book/testing.html](http://symfony.com/doc/current/book/testing.html) — все, что касается тестирования в Symfony.

## Evercode Related
Отлично! У нас уже есть определённый опыт по тому, как мы работаем с Symfony, по этому можно перейти конкретно к тем практикам, которые мы применяем в EvercodeLab.

Первое, стиль написание кода [https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style](https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style)
Второе, в целом имеет раскрывает лучшие практики (best practices) которые приняты у нас к работе. Да, они же приняты как лучшие практики Symfony комьюнити [http://symfony.com/doc/current/best_practices/index.html](http://symfony.com/doc/current/best_practices/index.html)

Для ускорения работы, мы используем свою небольшую сборку Symfony [https://github.com/EvercodeLab/symfony-skeleton](https://github.com/EvercodeLab/symfony-skeleton). В целом это тот же Symfony Standart Edition, просто с уже подключёнными бандлами, которые мы обычно используем в своей работе. Кроме того, там у нас есть набор полезных bash скриптов, которые упрощают развертывание проекта на локальной машине, а так же его обновление в процессе разработки. В данный момент у нас есть версия только для «обычного» стэка. В дальнейшем может появиться собранный набор конкретно для работы с API.

### Список бандлов с которыми мы имеем дело

* [SonataAdmin](https://sonata-project.org/bundles/admin/2-3/doc/index.html) – бандл который позволяет довольно быстро сгенерировать стандартную админ панель. Поддерживает большое количество различных функций и кастомизаций.
* [FosUserBundle](http://symfony.com/doc/master/bundles/FOSRestBundle/index.html) — бандл упрощающий (хотя иногда и усложняющий), работу с различным функционалом, связанным с пользователями. Регистрация, авторизация и прочее, пррочее.
* [PUGXMultiUserBundle](https://github.com/PUGX/PUGXMultiUserBundle) — данный бандл стыкуется с предыдущим и упрощает работу, если есть необходимость работать не с одной сущностью пользователей, а с несколькими.
* [KnpMenuBundle](http://symfony.com/doc/master/bundles/KnpMenuBundle/index.html) — облегчает генерацию меню для сайтов и позволяет это делать из одного файла (двух, если считать файл темплейтов)
* [KnpPaginatorBundle](https://github.com/KnpLabs/KnpPaginatorBundle) — генерируем постраничный вывод информации. Простая кастомизация. В комплекте шаблон для бутстрапа.
* [LiipImagineBundle](http://symfony.com/doc/master/bundles/LiipImagineBundle/index.html) — работа с картинками. Ресайз, наложение фильтров и еще много чего ещё.
* [VichUploaderBundle](https://github.com/dustin10/VichUploaderBundle) — как следует из названия, данный бандл работает с загрузкой файлов. Из удобных моментов стоит отметить возможность добавлять тип поля формы, который сразу будет выводить превью картинки, если есть какая-то загруженная.
* [DoctrineFixturesBundle](http://symfony.com/doc/master/bundles/DoctrineFixturesBundle/index.html) — работа с фикстурами данных (данными, которые загружаются в базу данных для примера)
* [DoctrineMigrationsBundle](http://symfony.com/doc/master/bundles/DoctrineMigrationsBundle/index.html) — по умолчанию, для сохранения процесса внесения изменений в структуру базы данных, мы используем миграции.
* [FOSRestBundle](http://symfony.com/doc/master/bundles/FOSRestBundle/index.html) — упрощаем и ускрояем разработку API. В целом полезный бандл, хотя есть нарекания, особенно на довольно серьёзную монструозность и комбайность.
* [NelmioApiDocBundle](https://github.com/nelmio/NelmioApiDocBundle/blob/master/Resources/doc/index.md) – данный бандл, в целом, работает в связке с предыдущим. Он добавляет возможность генерации АПИ документации на основе той информации, которую мы указываем в качестве DockBlock для каждого метода.
* [JMSSerializerBundle](https://github.com/schmittjoh/JMSSerializerBundle) — третий основной бандл, который помогает разрабатывать API.
* [FOSJsRoutingBundle](https://github.com/FriendsOfSymfony/FOSJsRoutingBundle/blob/master/Resources/doc/index.md) — позволяет генерировать правильные роуты прямо в JS.
* [DoctrineExtensions](https://github.com/Atlantic18/DoctrineExtensions) – добавляет крутой дополинетльный функционал для работы с Doctrine. Timestampable, Sluggable, etc.

## Aditional tools
Кроме основных тем, которые требуются непосредственно для понимания того, как работает симфония, есть ещё ряд дополнительных ресурсов, которые используются в нашей работе и влияют на общий стек.

* [Composer](https://getcomposer.org/doc/) — инструмент для управления зависимостями. Необходим как воздух, по этому очень важно знать, как с ним работать.
* [https://packagist.org/](https://packagist.org/), [http://knpbundles.com/](http://knpbundles.com/) – если у нас есть инструмент для управления зависимостями, то нам нужно где-то искать эти самые зависимости. Эти два сайта прекрасно справляются с этим. На первом можно найти вообще все, что можно «поставить» с помошью композера, второй больше Symfony related.
* [https://security.sensiolabs.org/](https://security.sensiolabs.org/), [https://insight.sensiolabs.com/](https://insight.sensiolabs.com/), [http://cs.sensiolabs.org/](http://cs.sensiolabs.org/) — SensioLabs, кроме непосредственно разработки Symfony так же занимается разработкой дополнительных утилит для своего фреймворка. Желательно со всеми ознакомится и иметь ввиду
* [http://capifony.org/](http://capifony.org/) — для деплоя (развертывания приложения на сервере), мы используем утилиту, которая называется capifony. Она полностью покрывает наши текущие необходимости по деплою.

## Advanced topics
Конечно, на этом ещё не всё ;) Этот раздел будет постепенно обновляться и дополняться различными статьями и книгами, которые подробнее рассказывают о тех или иных аспектах работы с Symfony

* [Create your own framework... on top of the Symfony2 Components](http://fabien.potencier.org/create-your-own-framework-on-top-of-the-symfony2-components-part-1.html) — серия постов Fabien Potencier в которой он рассказывает о том, как собрать свой собственный фреймворк из Symfony компонентов.
* [Symfony2 components overview](http://blog.servergrove.com/tag/symfony2-components/) — так же серия статей, которая более подробно рассматривает различные компоненты в отдельности.
* [The Symfony Components](http://symfony.com/doc/current/components/index.html) — если мы говорим про компоненты Symfony, то не стоит забывать и про официальную документацию. В ней можно найти исчерпывающую информацию по этим темам.
* [The Symfony Cookbook](http://symfony.com/doc/current/cookbook/index.html) — дополнительная документация с различными how-to, по тем или иным разделам.
* [A Year With Symfony](https://leanpub.com/a-year-with-symfony) — отличная книга, которая раскрывает некоторые моменты по разработке приложений с Symfony.
