---
layout: archive
title: "Exploration"
permalink: /blog/
author_profile: true
---

{% include base_path %}

{% for post in site.posts %}
  {% if post.categories contains "exploration" %}
  <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
    <div style="display: flex; align-items: center; margin-bottom: 2rem;">
      {% if post.image %}
        <div style="flex: 0 0 100px; margin-right: 1rem;">
          <img src="{{ post.image }}" alt="{{ post.title }}" style="width: 100px; border-radius: 4px;">
        </div>
      {% endif %}
      <div>
        <h2 class="archive__item-title no_toc" itemprop="headline">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="page__meta">
          📅 {{ post.date | date: "%Y-%m-%d" }} • 🕒 {{ post.read_time | default: "1 minute" }} read
        </p>
        <p class="archive__item-excerpt" itemprop="description">
          {{ post.excerpt | strip_html | truncatewords: 25 }}
        </p>
      </div>
    </div>
  </article>
  {% endif %}
{% endfor %}
