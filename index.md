---
layout: page
title: The Book of Knowledge (проект переехал)
tagline:
---
{% include JB/setup %}

**Эта версия TBoK устарела и больше не поддерживается. Актуальная версия [The Evercode Lab Book of Knowledge](https://github.com/EvercodeLab/thebookofknowledge) находится прямо в репозитории на github.**

The book of knowledge – база знаний компании [Evercode Lab](http://evercodelab.com). Любой участник команды, может добавить в проект данные, которые считает полезными для себя и других. Любой посетитель сайта может предложить свои добавления либо через комментарии, либо через issues или pull request на [github](https://github.com/EvercodeLab/thebookofknowledge).

The book of knowledge работает на [jekyll](https://github.com/mojombo/jekyll) с использованием [jekyllbootstrap](http://jekyllbootstrap.com/). Перед добавлением и изменением информации желательно ознакомиться.

Проект хостится на [github:pages](http://pages.github.com/).

## Техническое

* [Git](/pages/git.html)
* [Naming conventions](/pages/naming-conventions.html)
* [Deployment](/pages/deployment.html)
* [Utilities](/pages/utilities.html)
* [Symfony](pages/symfony.html)
* [Frameworks](/pages/frameworks.html)
* [The Pragmatic Programmer Quick Reference Guide](/pages/pragprogref.html)

## Редакторы

* [PHPStorm](/pages/phpstorm.html)
* [Sublime Text 2](/pages/sublime-text-2.html)

## General workflow

* [Миссия](/pages/mission.html)
* [«Че там по задачам?»](/pages/i-have-nothing-to-do.html)
* [Про технические задания](/pages/requirements-specification.html)
* [Задачи и работа с клиентами](/pages/working-with-clients.html)


## Education and Enlightenment

* [List of educational resources](/pages/educational-resources.html)
* [Design](/pages/design.html)
* [Books](/pages/books.html)
* [Learnable Programming](http://worrydream.com/LearnableProgramming/)

## In progress:

* [Tests](/pages/tests.html)
* [Creative Time](/pages/creative-time.html)
* [Environments](/pages/environments.html)
* [Must read](/pages/must-read.html)
* [Services](/pages/services.html)
* [Blogs](/pages/blogs.html)


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
