---
layout: page
title: The Book of Knowledge
tagline: 
---
{% include JB/setup %}


* [О проекте](/pages/about.html)
* [Git](/pages/git.html)
* [IDE](/pages/ide.html) - general page with links to subpages (concrete editors and IDEs)
* [Tests](/pages/tests.html)
* [Frameworks](/pages/frameworks.html) - general page with links to subpages (concrete editors and IDEs)
* [Coding standards](/pages/coding-standards.html)
* [Deployment](/pages/deployment.html)
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
