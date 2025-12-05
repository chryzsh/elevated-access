# Elevated Access

A technical blog for red team operations, penetration testing, and offensive security research. Built with Jekyll and hosted on GitHub Pages using the Moonwalk theme.

## Features

- Clean, dark mode by default
- Multi-author support
- Syntax highlighting for code blocks
- Responsive design
- Fast and minimal

## Adding a New Post

1. Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.md`
2. Add the front matter:

```markdown
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
author: yourname
categories: category1 category2
---

Your content here...
```

3. Write your content in Markdown
4. Commit and push to the repository

## Adding a New Author

1. Create a new file in `_authors/` with the format: `yourname.md`
2. Add the front matter:

```markdown
---
name: Your Full Name
short_name: yourname
bio: Brief bio about yourself
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
```

3. Use your `short_name` in the `author` field of your posts

## Local Development

1. Install Ruby and Bundler
2. Run `bundle install`
3. Run `bundle exec jekyll serve`
4. Visit `http://localhost:4000`

## Theme

This site uses the [Moonwalk](https://github.com/abhinavs/moonwalk) Jekyll theme with dark mode enabled by default.

## License

Content is licensed under CC BY-SA 4.0 unless otherwise specified.
