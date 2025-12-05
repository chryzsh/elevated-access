---
name: Example Author
short_name: example
bio: Red team operator and security researcher
---

# {{ page.name }}

{{ page.bio }}

## Articles by {{ page.name }}

<ul>
  {% for post in site.posts %}
    {% if post.author == page.short_name %}
      <li>
        <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
