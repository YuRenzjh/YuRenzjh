---
layout: page
title: 吐槽
description: 偶尔也需要发泄一下嘛
permalink: /rants/
---

<div class="posts-list">
{% assign rant_posts = site.posts | where_exp: "post", "post.categories contains '吐槽'" %}
{% for post in rant_posts %}
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
        {% endif %}
      {% endif %}
    </div>
    
    {% if post.excerpt %}
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
  </article>
{% endfor %}
</div>

{% if rant_posts.size == 0 %}
<div class="empty-state text-center mt-4">
  <p>😤 暂无吐槽内容，心情还不错嘛！</p>
</div>
{% endif %}
