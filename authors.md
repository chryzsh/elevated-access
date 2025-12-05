---
layout: page
title: Authors
permalink: /authors/
---

# Contributors

Meet the team behind TRS Blog.

<ul>
  {% for author in site.authors %}
    <li>
      <h3><a href="{{ author.url | relative_url }}">{{ author.name }}</a></h3>
      {% if author.bio %}
        <p>{{ author.bio }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
