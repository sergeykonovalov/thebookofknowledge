# С чего начать изучение Symfony

Фреймворк [Symfony](http://symfony.com/) является одниv из ключевых инструментов в Evercode Lab на данный момент. На нём строится бэкенд не менее 90% проектов наших клиентов.

Здесь мы хотим собрать ссылки на материалы для изучения всем, кто только начинает работать с фреймворком. Вероятно, что и опытные Symfony-разработчики найдут для себя что-то новое.

Если вам нужно обосновать выбор Symfony как основного фреймворка для разработки проекта перед начальством или самим собой, посмотрите статьи раздела [Symfony in 5 minutes](http://symfony.com/symfony_in_five_minutes) официальной документации.

## Начало

Начните изучение с [установки и настройки](http://symfony.com/doc/current/book/installation.html). Особое внимание уделите [проверке правильности конфигурации](http://symfony.com/doc/current/book/installation.html#checking-symfony-application-configuration-and-setup) и настройке прав на директории `cache` и `logs` (раздел Setting up Permissions), именно с последним на старте возникает больше всего проблем.

Следующий шаг — разобраться с [созданием новых страниц](http://symfony.com/doc/current/book/page_creation.html)

Для понимания того, как работает Symfony, обязательна к изучению статья [Symfony and HTTP Fundamentals](http://symfony.com/doc/current/book/http_fundamentals.html)

Основы работы с Symfony качественно и на примерах рассмотрены в скринкастах KnpUniversity:
* [Starting in Symfony2: Episode 1](https://knpuniversity.com/screencast/symfony2-ep1)
*  [Starting in Symfony2: Episode 2](https://knpuniversity.com/screencast/symfony2-ep2)
* [Starting in Symfony2: Episode 3](https://knpuniversity.com/screencast/symfony2-ep3)
*  [Starting in Symfony2: Episode 4](https://knpuniversity.com/screencast/symfony2-ep4)

В видео расскано о всех моментах повседневной работы с Symfony. Рекомендуется также посмотреть исходный код и выполнить задания. Для удобства есть транскрипты.

Помимо основных эпизодов есть и [ряд других скринкастов по Symfony](https://knpuniversity.com/tracks/symfony), которые стоит посмотреть. Компания обеспечивает сотрудников доступом ко всем нужным материалам.

## Основная документация

* различные аспекты [работы с контроллерами](http://symfony.com/doc/current/book/controller.html)
* как создавать [правильные пути](http://symfony.com/doc/current/book/routing.html)
* научиться [работать с Doctrine](http://symfony.com/doc/current/book/doctrine.html). Важно понять, что ORM это не Active Record. В сущностях мы храним минимум бизнес логики, обычно большая её часть находится в сервисном слое
*  [официальный сайт Doctrine](http://docs.doctrine-project.org/projects/doctrine-orm/en/latest/)
* для [работы с шаблонами](http://symfony.com/doc/current/book/templating.html) Symfony использует [twig](http://twig.sensiolabs.org/documentation)

Есть ещё несколько очень важных тем, которые стоит прочитать в документации:

* [работа с формами](http://symfony.com/doc/current/book/forms.html)
* [security](http://symfony.com/doc/current/book/security.html) — security
* [переводы](http://symfony.com/doc/current/book/translation.html) — переводы
* [работа с Service Container](http://symfony.com/doc/current/book/service_container.html)
* все, что касается [тестирования в Symfony](http://symfony.com/doc/current/book/testing.html)

## Evercode Related

У нас в Evercode Lab уже есть определённый опыт по работе с Symfony, далее немного об этом.

* [стиль написание кода](https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style) и наши пополняемые best practices
* мы разделяем [Symfony Best Practices](http://symfony.com/doc/current/best_practices/index.html)
* для ускорения работы мы используем [свою небольшую сборку Symfony](https://github.com/EvercodeLab/symfony-skeleton). Это тот же Symfony Standart Edition с уже подключенными бандлами, которые мы обычно используем в своей работе. Там же есть набор полезных bash скриптов, которые упрощают развертывание проекта на локальной машине и его обновление в процессе разработки. В данный момент у нас есть версия только для «обычного» стэка. В дальнейшем может появиться собранный набор конкретно для работы с API.

### Список бандлов с которыми мы имеем дело

* [SonataAdmin](https://sonata-project.org/bundles/admin/2-3/doc/index.html) — позволяет довольно быстро сгенерировать стандартную админ панель
* [FosUserBundle](http://symfony.com/doc/master/bundles/FOSRestBundle/index.html) — иногда упрощающий (иногда и усложняющий) работу с различным функционалом, связанным с пользователями. Регистрация, авторизация и прочее.
* [PUGXMultiUserBundle](https://github.com/PUGX/PUGXMultiUserBundle) — стыкуется с предыдущим и упрощает работу, если есть необходимость работать не с одной сущностью пользователей, а с несколькими.
* [KnpMenuBundle](http://symfony.com/doc/master/bundles/KnpMenuBundle/index.html) — облегчает генерацию меню для сайтов и позволяет это делать из одного файла (двух, если считать файл темплейтов)
* [KnpPaginatorBundle](https://github.com/KnpLabs/KnpPaginatorBundle) — генерируем постраничный вывод информации. Простая кастомизация. В комплекте шаблон для бутстрапа.
* [LiipImagineBundle](http://symfony.com/doc/master/bundles/LiipImagineBundle/index.html) — работа с картинками. Ресайз, наложение фильтров и много чего ещё.
* [VichUploaderBundle](https://github.com/dustin10/VichUploaderBundle) — работает с загрузкой файлов. Из удобных моментов: возможность добавлять тип поля формы, который сразу будет выводить превью картинки, если она уже загружена
* [DoctrineFixturesBundle](http://symfony.com/doc/master/bundles/DoctrineFixturesBundle/index.html) — работа с фикстурами данных
* [DoctrineMigrationsBundle](http://symfony.com/doc/master/bundles/DoctrineMigrationsBundle/index.html) — мы используем миграции для базы данных на всех проектах
* [FOSRestBundle](http://symfony.com/doc/master/bundles/FOSRestBundle/index.html) — упрощаем и ускрояем разработку API. Полезный бандл, но есть нарекания на довольно серьёзную монструозность и комбайность
* [NelmioApiDocBundle](https://github.com/nelmio/NelmioApiDocBundle/blob/master/Resources/doc/index.md) – работает в связке с предыдущим. Добавляет возможность генерации документации к API на основе той информации, которую мы указываем в качестве DockBlock для каждого метода.
* [JMSSerializerBundle](https://github.com/schmittjoh/JMSSerializerBundle) — третий основной бандл, который помогает разрабатывать API
* [FOSJsRoutingBundle](https://github.com/FriendsOfSymfony/FOSJsRoutingBundle/blob/master/Resources/doc/index.md) — позволяет генерировать правильные роуты прямо в JS
* [DoctrineExtensions](https://github.com/Atlantic18/DoctrineExtensions) – добавляет крутой дополинетльный функционал для работы с Doctrine. Timestampable, Sluggable, etc.

## Additional tools

Есть ещё ряд дополнительных ресурсов и инструментов, которые используются в нашей работе. SensioLabs, кроме непосредственно разработки Symfony так же занимается разработкой дополнительных утилит для своего фреймворка. Желательно со всеми ознакомится и иметь в виду.

* [Composer](https://getcomposer.org/doc/) — незаменимый инструмент для управления зависимостями
* [Packagist](https://packagist.org/), [KnpBundles](http://knpbundles.com/) – ресурсы для поиска библиотек и бандлов с готовым функционалом
* [https://security.sensiolabs.org/](https://security.sensiolabs.org/) — сервис для проверки наличия уязвимостей в зависимостях проекта
*  [https://insight.sensiolabs.com/](https://insight.sensiolabs.com/) — анализ Symfony проектов
* [http://cs.sensiolabs.org/](http://cs.sensiolabs.org/) — автоматическая проверка code style
* [Capifony](http://capifony.org/) — инструмент для автоматизации деплоя Symfony приложений. На данный момент полностью покрывает наши текущие нужды.

## Advanced topics

* [Create your own framework... on top of the Symfony2 Components](http://fabien.potencier.org/create-your-own-framework-on-top-of-the-symfony2-components-part-1.html) — серия постов Fabien Potencier в которой он рассказывает о том, как собрать свой собственный фреймворк из Symfony компонентов.
* [Symfony2 components overview](http://blog.servergrove.com/tag/symfony2-components/) — серия статей, которая более подробно рассматривает различные компоненты
* [The Symfony Components](http://symfony.com/doc/current/components/index.html) — официальная документация по компонентам
* [The Symfony Cookbook](http://symfony.com/doc/current/cookbook/index.html) — дополнительная документация с различными how-to, по тем или иным разделам.
* [A Year With Symfony](https://leanpub.com/a-year-with-symfony) — отличная книга, которая раскрывает некоторые моменты по разработке приложений с Symfony.
