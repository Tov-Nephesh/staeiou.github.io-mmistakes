---
title: Academic Articles
permalink: /articles/
---

<ul>
  {% for post in site.categories.articles %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
