---
layout: default
---

<div>
  <div>
    {% for post in site.posts limit: 1 %}
    <article>
      <section class="line-h15 link-title">
        <span class="h2"><a href="{{ post.url }}">{{ post.title }}</a></span>
      </section>
      <section class="px1 h5 line-h15 color-title">
        <span>
          <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
        </span>
        {% if post.tags %}
        <span class="link-title">
          {% for tag in post.tags %}
          <a href="/tags.html#{{ tag }}" title="{{ tag }}">#{{ tag }}</a>
          {% endfor %}
        </span>
      {% endif %}
      </section>
      <section class="myn2 px2 h4">
        {{ post.content }}
      </section>
      <div class="my4 h1 center color-divider link-divider divider">
        <span class="p4">
          {% for post in site.posts limit:1 offset:1 %}
          <a href="{{ post.url }}"><i class="fa fa-chevron-left"></i></a>
          {% endfor %}
        </span>
        <span class="p4"> <i class="fa fa-circle"></i> </span>
      </div>
    </article>
    {% endfor %}
  </div>
  <ul class="myn2 h4 line-h15">
    {% capture year %}{{ site.time | date:"%Y"}}{% endcapture %}
    {% for post in site.posts offset:1 %}
      {% capture y %}{{ post.date | date:"%Y"}}{% endcapture %}
      {% if year != y %}
        {% break %}
      {% endif %}
      <li class="list-none list-seperator color-strong">Happend earlier this year</li>
      <li class="ml1 line-h15 color-list link-list list-none">
        <div class="clearfix">
          <div class="col pr2">
            <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
          </div>
          <div class="col col-9">
            <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
          </div>
        </div>
      </li>
    {% endfor %}
    <li class="list-none list-seperator"><a href="/archive.html">Posts Archive</a></li>
  </ul>
</div>
