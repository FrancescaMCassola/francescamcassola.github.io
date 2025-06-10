---
layout: default
title: Blog
permalink: /it/blog/
---

<div class="main-post-list">
  <ol class="post-list">
    {% assign posts = site.posts | where:"lang", "it" %}
    {% for post in posts %}
    <li>
      <h2 class="post-list__post-title post-title">
        <a href="{{ post.url }}" title="Leggi l'articolo completo: {{ post.title }}">{{ post.title }}</a>
      </h2>
      <p class="excerpt">{{ post.content | strip_html | strip_newlines | truncate: 250 }}&hellip;</p>
      <div class="post-list__meta">
        <time datetime="{{ post.date | date: date_to_xmlschema }}" class="post-list__meta--date date">
          {{ post.date | date: "%F" }}
        </time>
        &#8226;
        <span class="post-list__meta--tags tags">{{ post.tags | join:' ' }}</span>
        <a class="btn-border-small" href="{{ post.url }}">Leggi tutto</a>
      </div>
      <hr class="post-list__divider" />
    </li>
    {% endfor %}
  </ol>
</div>
