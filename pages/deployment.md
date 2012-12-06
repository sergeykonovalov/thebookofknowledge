---
layout: page
title: "Deployment"
description: ""
---
{% include JB/setup %}

## Capistrano

Применяется как для RoR приложений, так и для PHP проектов, под нужды которых легко адаптируется.

Ссылки:

* https://github.com/capistrano/capistrano/wiki/
* [Capistrano for PHP Applications Deployment (ZFConf)](https://speakerdeck.com/u/romalapin/p/capistrano-for-php-applications-deployment)
* [Capistrano for PHP Applications Deployment (DevConf)](https://speakerdeck.com/u/romalapin/p/capistrano-for-php-applications-deployemnt-devconf-version)

## Capifony

[Capifony](http://capifony.org/) - наше все для проектов на Symfony2.

[Multistage Extension](http://capifony.org/cookbook/using-the-multistage-extension.html) используется практически на всех проектах. `Staging` – для деплоя на тестовый сервак на время разработки. `Production` для деплоя в продакшен.

`set :default_stage, "staging"` делает деплой на тестовый сервак дефолтным для команды `cap deploy`. Для production надо будет указать явно: `cap production deploy`.

Болванки для файлов конфига и .htaccess для полноценной работы всех задач можно найти здесь: <https://gist.github.com/3143253>

Кэш убран из `set :shared_children` из-за частых проблем с правами даже при рекомендованных настройках setfacl. И по логике он может различаться для разных релизов, поэтому это не так и плохо.

Желательно использовать миграции как можно раньше, это позволит обновлять базу через capifony.

Полезные команды:

{% highlight bash %}
cap -vT  – показывает все доступные команды
cap deploy - gogogo!
cap deploy:rollback – shit! we're fucked up! abort the mission
cap symfony:.... - команды консоли symfony
cap deploy:migrate - прогнать миграции
cap deploy:web:disable - отключить сервис и показать maintanence.html
cap deploy:web:enable - включить сервис
{% endhighlight %}


## Автоматизация добавления задач в cron

* gem [Whenever](https://github.com/javan/whenever)
* [Symfony2, Deploy и Cron](http://blog.evercodelab.com/symfony2-and-cron/)

## Простой, быстрый, но ограниченный способ

[Описание в блоге Evercode Lab](http://blog.evercodelab.com/easiest-deployment-with-git-and-ssh/)

{% highlight bash %}
git archive --format=tar origin/master | gzip -9c | ssh user@yourserver.com "cd /var/www; tar xvzf -"
{% endhighlight %}

Команду теоретически можно дополнить другими директивами и сохранить в отдельный файл.

Способ не рекомендуется для постоянного использования, но может быть применен в случае возникновения проблем с Capistrano из-за ограничений хостинга или других подобных проблем.


## Phing

<http://www.phing.info/trac/>

Мощный, но сложный инструмент. 


## Полезно почитать

* [Infrastructure Debt](http://www.littlehart.net/atthekeyboard/2011/11/03/infrastructure-debt/)
* [Advanced server definitions in Capistrano](http://railsware.com/blog/2011/11/02/advanced-server-definitions-in-capistrano/)