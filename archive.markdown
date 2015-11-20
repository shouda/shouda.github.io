---
title: archive
layout: page
---

<ul class="myn2 h4 line-h15">
  {% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
  {% assign year = y %}
  <li class="list-none list-seperator">{{ y }}</li>
  {% endif %}
  <li class="ml1 line-h15 color-list link-list list-none">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
