---
layout: page
title: 文章
description: 所有文章列表
permalink: /posts/
---

<div class="posts-list">
{% for post in site.posts %}
  <article class="post-card">
    <div class="post-card-header">
      <h2 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
    </div>
    
    <div class="post-card-meta">
      <span class="post-card-date">📅 {{ post.date | date: "%Y年%m月%d日" }}</span>
      
      {% if post.mood %}
        {% assign mood_info = site.moods[post.mood] %}
        {% if mood_info %}
          <a href="{{ '/mood/' | append: post.mood | append: '/' | relative_url }}" class="mood-badge {{ mood_info.class }}">
            {{ mood_info.emoji }}{{ post.mood }}
          </a>
        {% else %}
          <span class="mood-badge mood-calm">💙{{ post.mood }}</span>
        {% endif %}
      {% endif %}
    </div>
    
    {% if post.excerpt %}
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
    
    {% if post.categories.size > 0 %}
      <div class="post-card-categories">
        {% for category in post.categories %}
          <span class="category-tag">{{ category }}</span>
        {% endfor %}
      </div>
    {% endif %}
  </article>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<div class="empty-state text-center mt-4">
  <p>暂无文章，敬请期待！</p>
</div>
{% endif %}
