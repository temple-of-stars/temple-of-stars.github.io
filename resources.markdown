---
layout: page
title: Resources
permalink: /resources/
---

<div class="resources-intro">
  <p>A curated collection of readings, videos, and other media that explore the intersection of science, philosophy, consciousness, and cosmic wonder.</p>
</div>

## Reading List

<div class="resource-list">
  {% assign reading_list = site.data.resources.books %}
  {% for item in reading_list %}
  <div class="resource-item">
    <h3 class="resource-title">{{ item.title }}</h3>
    <div class="resource-meta">
      <span class="resource-author">{{ item.author }}</span>
      {% if item.year %}
      <span class="resource-year">({{ item.year }})</span>
      {% endif %}
    </div>
    <p class="resource-description">{{ item.description }}</p>
    {% if item.tags %}
    <div class="resource-tags">
      {% for tag in item.tags %}
      <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    {% endif %}
  </div>
  {% endfor %}
</div>

## Media & Videos

<div class="resource-list">
  {% assign media_list = site.data.resources.media %}
  {% for item in media_list %}
  <div class="resource-item">
    <h3 class="resource-title">
      {% if item.url %}
      <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
      {% else %}
      {{ item.title }}
      {% endif %}
    </h3>
    <div class="resource-meta">
      <span class="resource-type">{{ item.type }}</span>
      {% if item.author %}
      <span class="resource-author">• {{ item.author }}</span>
      {% endif %}
      {% if item.year %}
      <span class="resource-year">• {{ item.year }}</span>
      {% endif %}
    </div>
    <p class="resource-description">{{ item.description }}</p>
    {% if item.tags %}
    <div class="resource-tags">
      {% for tag in item.tags %}
      <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    {% endif %}
  </div>
  {% endfor %}
</div>
