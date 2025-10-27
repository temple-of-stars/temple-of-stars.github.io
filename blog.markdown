---
layout: page
title: Blog
permalink: /blog/
---

<section>
  <div class="section-title-center">
    <h1 class="section-title">Blog</h1>
  </div>

  <div class="section-list">
        {% for post in site.posts %}
        <div class="list-item">
          <h2 class="list-item-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <div class="list-item-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%B %-d, %Y" }}
            </time>
          </div>
          {% if post.excerpt %}
          <p class="list-item-description">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
          {% endif %}
          <a href="{{ post.url | relative_url }}" class="list-item-link">Read more →</a>
        </div>
          {% endfor %}
  </div>
</section>

