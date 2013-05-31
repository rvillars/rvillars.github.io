---
layout: page
title: Big Endian
tagline: The JVM blog
---
{% include JB/setup %}

{% for post in site.posts limit:10 %}
  <div class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <div class="post-date">{{ post.date | date: "%B %d, %Y" }}</div>
    {{ post.content | split:'<!--break-->' | first }}
    {% if post.content contains '<!--break-->' %}
      <a href="{{ post.url }}">Read more</a>
    {% endif %}
  </div>
{% endfor %}


