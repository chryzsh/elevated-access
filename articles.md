---
layout: page
title: Articles
permalink: /articles/
---

# All Articles

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      {% if post.author %}
        <p class="post-author">By {{ post.author }}</p>
      {% endif %}
      {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
