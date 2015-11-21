---
title: tags
layout: page
---

<div id='tag_cloud'>
{% for tag in site.tags %}
<a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endfor %}
</div>

<ul class="myn2 h4 line-h15">
  {% for tag in site.tags %}
  <li class="list-none list-seperator color-strong" id="{{ tag[0] }}">{{ tag[0] }}</li>
  {% for post in tag[1] %}
  <li class="ml1 line-h15 color-list link-list list-none">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
  {% endfor %}
  {% endfor %}
</ul>

<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.min.js" type="text/javascript" charset="utf-8"></script>
<script src="/media/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script>
<script language="javascript">
  $.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
    color: {start: '#efb6c4', end: '#ff3333'}
  };

  $(function () {
    $('#tag_cloud a').tagcloud();
  });
</script>
