---
layout: page
---
{% include JB/setup %}

<div class="hero-unit">
  <h1>Big Endian</h1>
  <p>The JVM Blog</p>
</div>

{% for post in site.posts limit:10 %}
  <div class="bs-docs-example">
    <div><h2>{{ post.title }} <small>{{ post.tagline }}</small></h2></div>
    <div class="post-full"> 
      <div class="date"><span>{{ post.date | date: "%B %d, %Y" }}</span></div>
      <div class="content">
        {{ post.content | split:'<!--break-->' | first }}
        {% if post.content contains '<!--break-->' %}
          <a href="{{ post.url }}">Read more</a>
        {% endif %}
      </div>
    </div>
  </div>
  <hr class="bs-docs-separator"></hr>
{% endfor %}


