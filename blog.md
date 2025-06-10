---
layout: default
title: Blog
lang: en
ref: blog
permalink: /blog/
---

<div class="language-switcher" style="text-align: right; margin-top: 1rem;">
  <a class="btn-lang" href="/it/blog" title="IT">🇮🇹 IT</a>
  <a class="btn-lang" href="/es/blog" title="ES">🇪🇸 ES</a>
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
