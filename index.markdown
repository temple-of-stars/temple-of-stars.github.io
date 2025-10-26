---
layout: page
title: Home
---

<div class="hero-section">
  <h1 class="hero-title">Welcome to the Temple of Stars</h1>
  <p class="hero-subtitle">A sanctuary for those who look up at the stars with wonder</p>
</div>

<div class="intro-section">
  <p class="intro-text">
    We are scientists, artists, and thinkers building a new kind of spiritual community grounded in awe. The Temple of Stars is a place where science meets spirituality, where the rational and the mystical coexist in harmony. We believe that understanding the cosmos deepens our sense of wonder, and that wonder itself is a form of reverence.
  </p>
  <p class="intro-text">
    Here, we explore the vast questions that unite us: What is consciousness? What is our place in the universe? How do we find meaning in a cosmos of incomprehensible scale? Through dialogue, reflection, and shared experience, we seek not answers but better questions—and the courage to sit with uncertainty.
  </p>
  <p class="intro-text">
    Join us in contemplating the infinite, celebrating the scientific method, and honoring the profound mystery of existence. Together, we build a temple not of stone, but of shared curiosity and cosmic perspective.
  </p>
</div>

<section class="recent-posts">
  <h2 class="section-title">Recent Reflections</h2>
  
  <div class="post-grid">
    {% for post in site.posts limit:3 %}
    <article class="post-card">
      <h3 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <div class="post-card-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%B %-d, %Y" }}
        </time>
      </div>
      {% if post.excerpt %}
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
      <a href="{{ post.url | relative_url }}" class="post-card-link">Read more →</a>
    </article>
    {% endfor %}
  </div>
  
  <div class="section-cta">
    <a href="{{ '/blog' | relative_url }}" class="btn btn-primary">View All Posts</a>
  </div>
</section>

<section class="featured-resources">
  <h2 class="section-title">Featured Resources</h2>
  
  <div class="resource-preview-grid">
    {% assign featured_books = site.data.resources.books | slice: 0, 2 %}
    {% for item in featured_books %}
    <div class="resource-preview-card">
      <h4 class="resource-preview-title">{{ item.title }}</h4>
      <p class="resource-preview-author">{{ item.author }}</p>
      <p class="resource-preview-description">{{ item.description | truncatewords: 20 }}</p>
    </div>
    {% endfor %}
    
    {% assign featured_media = site.data.resources.media | slice: 0, 1 %}
    {% for item in featured_media %}
    <div class="resource-preview-card">
      <h4 class="resource-preview-title">
        <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
      </h4>
      <p class="resource-preview-author">{{ item.author }}</p>
      <p class="resource-preview-description">{{ item.description | truncatewords: 20 }}</p>
    </div>
    {% endfor %}
  </div>
  
  <div class="section-cta">
    <a href="{{ '/resources' | relative_url }}" class="btn btn-secondary">Explore All Resources</a>
  </div>
</section>
