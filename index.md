---
layout: page
title: Big Endian
tagline: The JVM blog
---
{% include JB/setup %}

{% for post in site.posts limit:10 %}
  <div>
    <div class="page-header"><h1>{{ post.title }}<small>{{ post.tagline }}</small></h1></div>
    <div class="date">{{ post.date | date: "%B %d, %Y" }}</div>
    {{ post.content | split:'<!--break-->' | first }}
    {% if post.content contains '<!--break-->' %}
      <a href="{{ post.url }}">Read more</a>
    {% endif %}
  </div>
{% endfor %}


