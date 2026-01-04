---
layout: page
title: 闲聊
description: 轻松愉快的日常碎片
permalink: /chats/
---

<div class="posts-list">
{% assign chat_posts = site.posts | where_exp: "post", "post.categories contains '闲聊'" %}
{% for post in chat_posts %}
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

{% if chat_posts.size == 0 %}
<div class="empty-state text-center mt-4">
  <p>💬 暂无闲聊内容，快来写点什么吧！</p>
</div>
{% endif %}
