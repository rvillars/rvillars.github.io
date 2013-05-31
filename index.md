---
layout: page
title: Big Endian
tagline: The JVM blog
---
{% include JB/setup %}

{% for post in site.posts limit:10 %}
  <div>
    <div><h2>{{ post.title }}</h2><small>{{ post.tagline }}</h3></small>
    <div class="post-full date">{{ post.date | date: "%B %d, %Y" }}</div>
    {{ post.content | split:'<!--break-->' | first }}
    {% if post.content contains '<!--break-->' %}
      <a href="{{ post.url }}">Read more</a>
    {% endif %}
  </div>
{% endfor %}


