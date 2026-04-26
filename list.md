---
layout: default
title: 犬種一覧
permalink: /list/
---

<style>
  /* 同様のスタイル */
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  header.site-header, .site-header, .page-title, h1:first-of-type { display: none !important; }
  .custom-header { background: white; padding: 15px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }
  .section-title { text-align: center; font-size: 18px; font-weight: bold; margin: 25px 0 5px; color: #333; }
  .container { padding: 10px 15px 40px; }
  
  /* 犬種名のカードデザイン */
  .breed-card { 
    display: flex; 
    align-items: center; 
    background: white; 
    border-radius: 10px; 
    box-shadow: 0 2px 6px rgba(0,0,0,0.06); 
    margin-bottom: 8px; 
    padding: 12px 15px; 
    text-decoration: none; 
    color: #333; 
  }
  .breed-name { font-size: 15px; font-weight: bold; flex: 1; }
  .breed-arrow { color: #ffcc00; font-size: 12px; }
</style>

<div class="custom-header">
  <div id="category-title" class="custom-title">犬種リスト</div>
</div>

<div class="section-title">あいうえお順</div>

<div id="breed-list" class="container">
  {% assign sorted_posts = site.posts | sort: "title" %}
  {% for post in sorted_posts %}
    <a href="{{ post.url | relative_url }}" 
       class="breed-card" 
       style="display:none;" 
       data-cat="{{ post.categories | join: ',' }}">
      <span class="breed-name">{{ post.title }}</span>
      <span class="breed-arrow">詳細を見る ▶</span>
    </a>
  {% endfor %}
</div>

<script>
  const urlParams = new URLSearchParams(window.location.search);
  const selectedCat = urlParams.get('cat');
  if (selectedCat) {
    document.getElementById('category-title').innerText = selectedCat;
    const items = document.querySelectorAll('.breed-card');
    items.forEach(item => {
      if (item.getAttribute('data-cat').split(',').includes(selectedCat)) {
        item.style.display = 'flex';
      }
    });
  }
</script>

<div style="text-align: center; padding-bottom: 40px;">
  <a href="javascript:history.back()" style="color: #888; font-size: 14px; text-decoration: none;">← 前の画面に戻る</a>
</div>
