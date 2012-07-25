---
layout: page
title: The Book of Knowledge
tagline: 
---
{% include JB/setup %}

The book of knowledge – база знаний компании [Evercode Lab](http://www.evercodelab.com). Любой участник команды, может добавить в проект данные, которые считает полезными для себя и других. Любой посетитель сайта может предложить свои добавления либо через комментарии, либо через issues или pull request на github.

The book of knowledge работает на [jekyll](https://github.com/mojombo/jekyll) с использованием [jekyllbootstrap](http://jekyllbootstrap.com/). Перед добавлением и изменением информации желательно ознакомиться.

Проект хостится на [github:pages](http://pages.github.com/).


* [Git](/pages/git.html)
* [Naming conventions](/pages/naming-conventions.html)
* [Deployment](/pages/deployment.html)
* [Utilities](/pages/utilities.html)
* [List of educational resources](/pages/educational-resources.html)
* [Design](/pages/design.html)

In progress:

* [IDE](/pages/ide.html) - general page with links to subpages (concrete editors and IDEs)
* [Tests](/pages/tests.html)
* [Frameworks](/pages/frameworks.html) - general page with links to subpages (concrete editors and IDEs)
* [Creative Time](/pages/creative-time.html)
* [Environments](/pages/environments.html)
* [Must read](/pages/must-read.html)
* [Services](/pages/services.html)
* [Blogs](/pages/blogs.html)
* [Books](/pages/books.html)


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
