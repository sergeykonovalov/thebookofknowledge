---
layout: page
title: The Book of Knowledge
tagline: 
---
{% include JB/setup %}


* [О проекте](/pages/about.html)
* [Git](/pages/git.html)


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
