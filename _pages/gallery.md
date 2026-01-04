---
layout: page
title: 相册
description: 用镜头记录生活的美好瞬间
permalink: /gallery/
---

<div class="gallery-grid">
  <!-- 相册图片示例 -->
  <!-- 将图片放入 /assets/gallery/ 目录后，在此处添加 img 标签 -->
  <!-- 示例：<img src="{{ '/assets/gallery/photo.jpg' | relative_url }}" alt="描述"> -->
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">📷</span>
      <span class="placeholder-text">示例图片 1</span>
    </div>
    <div class="gallery-item-caption">美好的一天</div>
  </div>
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">🌅</span>
      <span class="placeholder-text">示例图片 2</span>
    </div>
    <div class="gallery-item-caption">阳光明媚</div>
  </div>
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">🌙</span>
      <span class="placeholder-text">示例图片 3</span>
    </div>
    <div class="gallery-item-caption">静谧时光</div>
  </div>
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">✨</span>
      <span class="placeholder-text">示例图片 4</span>
    </div>
    <div class="gallery-item-caption">灵感瞬间</div>
  </div>
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">🌸</span>
      <span class="placeholder-text">示例图片 5</span>
    </div>
    <div class="gallery-item-caption">温柔岁月</div>
  </div>
  
  <div class="gallery-item gallery-placeholder">
    <div class="placeholder-content">
      <span class="placeholder-icon">🕊️</span>
      <span class="placeholder-text">示例图片 6</span>
    </div>
    <div class="gallery-item-caption">淡淡忧伤</div>
  </div>
</div>

<div class="text-center mt-3">
  <p class="text-muted">
    📷 将你的照片放入 <code>/assets/gallery/</code> 目录，然后在此页面添加对应的 <code>&lt;img&gt;</code> 标签
  </p>
</div>

<style>
.gallery-placeholder {
  background: linear-gradient(135deg, var(--blue-calm), var(--blue-joy));
  display: flex;
  align-items: center;
  justify-content: center;
}
.placeholder-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  color: white;
}
.placeholder-icon {
  font-size: 3rem;
}
.placeholder-text {
  font-size: 0.9rem;
  opacity: 0.8;
}
</style>
