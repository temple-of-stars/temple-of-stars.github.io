---
layout: page
title: Resources
permalink: /resources/
---

<section>
  <div class="section-title-center">
    <h1 class="section-title">Resources</h1>
    <p class="section-subtitle">Curated materials for cosmic contemplation</p>
  </div>

  <div class="section-highlight">
    <p>A collection of readings, videos, and other media that explore the intersection of science, philosophy, consciousness, and cosmic wonder.</p>
  </div>
</section>

<section>
  <div class="section-title-center">
    <h2 class="section-title">Reading List</h2>
  </div>

  <div class="section-list">
    {% assign reading_list = site.data.resources.books %}
    {% for item in reading_list %}
    <div class="list-item">
      <h3 class="list-item-title">{{ item.title }}</h3>
      <div class="list-item-meta">
        <span class="resource-author">{{ item.author }}</span>
        {% if item.year %}
        <span> • {{ item.year }}</span>
        {% endif %}
      </div>
      <p class="list-item-description">{{ item.description }}</p>
      {% if item.tags %}
      <div class="tag-list">
        {% for tag in item.tags %}
        <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>

<section>
  <div class="section-title-center">
    <h2 class="section-title">Media & Videos</h2>
  </div>

  <div class="section-list">
    {% assign media_list = site.data.resources.media %}
    {% for item in media_list %}
    <div class="list-item">
      <h3 class="list-item-title">
        {% if item.url %}
        <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
        {% else %}
        {{ item.title }}
        {% endif %}
      </h3>
      <div class="list-item-meta">
        <span class="type-badge">{{ item.type }}</span>
        {% if item.author %}
        <span> • {{ item.author }}</span>
        {% endif %}
        {% if item.year %}
        <span> • {{ item.year }}</span>
        {% endif %}
      </div>
      <p class="list-item-description">{{ item.description }}</p>
      {% if item.tags %}
      <div class="tag-list">
        {% for tag in item.tags %}
        <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>
