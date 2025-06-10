---
layout: simple-page
title: Blog
permalink: /en/blog/
---
<div class="lang-switch" style="text-align: right; margin-bottom: 1em;">
  <a href="{{ '/it/blog/' | relative_url }}"><img src="{{ '/assets/images/flag-it.svg' | relative_url }}" alt="Italiano" width="24"></a>
  <a href="{{ '/es/blog/' | relative_url }}"><img src="{{ '/assets/images/flag-es.svg' | relative_url }}" alt="Español" width="24"></a>
</div>

{% assign blog_posts = site.categories.blog-en | sort: 'date' | reverse %}

{% for post in blog_posts %}
  <article class="blog-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="blog-date">{{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    <a href="{{ post.url | relative_url }}" class="read-more">Read more</a>
    <hr>
  </article>
{% endfor %}

Force rebuild
