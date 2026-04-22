---
title: Blog
---

<section class="section-card blog-list">
  <p class="eyebrow">Writing</p>
  <h1>Blog</h1>
  <p class="section-intro">Notes, updates, and longer-form writing in Markdown.</p>
  <ul class="blog-posts">
    {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <p class="muted">{{ post.date | date: "%B %d, %Y" }}</p>
      {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>
