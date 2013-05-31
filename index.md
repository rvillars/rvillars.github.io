---
layout: page
title: Big Endian
tagline: The JVM blog
---
{% include JB/setup %}

{% for post in site.posts limit:10 %}
  <div class="post-preview">
    <div><h2>{{ post.title }}</h2><h3>{{ post.tagline }}</h3></div>
    <div class="post-date"><b>{{ post.date | date: "%B %d, %Y" }}</b></div>
    {{ post.content | split:'<!--break-->' | first }}
    {% if post.content contains '<!--break-->' %}
      <a href="{{ post.url }}">Read more</a>
    {% endif %}
  </div>
{% endfor %}


