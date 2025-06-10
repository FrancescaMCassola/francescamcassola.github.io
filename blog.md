---
layout: blog
title: Blog
lang: en
ref: blog
permalink: /blog/
---

<div class="language-switcher" style="text-align: right; margin-top: 1rem;">
  <a href="/it/blog">🇮🇹 IT</a> |
  <a href="/es/blog">🇪🇸 ES</a>
</div>

{% for post in site.posts %}
  {% if post.lang == "en" %}
  <div class="post-preview">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
    <hr />
  </div>
  {% endif %}
{% endfor %}
