---
layout: default
title: Blog
lang: en
ref: blog
permalink: /blog/
---

{% for post in site.posts %}
  {% if post.lang == "en" %}
  <div class="post-preview">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
    <hr />
  </div>
  {% endif %}
{% endfor %}
