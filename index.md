---
layout: page
title: UIX
tagline: 프론트엔드 개발을 위하여
---

<ul class="posts">
  {% for post in site.posts %}
    <li><span class="date_num">{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


