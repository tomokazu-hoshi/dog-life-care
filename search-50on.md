---
layout: default
title: 50音検索
permalink: /Search-50on/
---

<style>
  /* 1. 不要なタイトルを強制的に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  
  /* シンプルなタイトル表示（線は一切なし） */
  .section-title { 
    text-align: center; 
    font-size: 22px; 
    font-weight: bold; 
    margin: 40px 0 20px; 
    color: #333; 
  }

  /* グリッドレイアウト（犬種図鑑のボタンサイズに合わせました） */
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(2, 1fr); 
    gap: 12px; 
    padding: 0 15px 50px; 
    max-width: 400px; 
    margin: 0 auto; 
  }

  .grid-card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); 
    padding: 20px 5px; 
    text-decoration: none; 
    color: #333; 
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid #eee;
    font-weight: bold;
    font-size: 18px;
    min-height: 80px; /* 押しやすい高さ */
  }
  
  .grid-card:active { background-color: #fff9f0; transform: scale(0.95); }

</style>

<!-- 余計なdivは使わず、ただの文字として配置 -->
<div class="section-title">🔤 50音検索</div>

<div class="grid-container">
  {% assign lines = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
  {% for line in lines %}
    <a href="{{ '/list/?cat=' | append: line | relative_url }}" class="grid-card">
      {{ line }}
    </a>
  {% endfor %}
</div>

<div style="text-align: center; padding-bottom: 50px;">
  <a href="{{ '/dog-search/' | relative_url }}" style="color: #888; font-size: 14px; text-decoration: none;">← 検索に戻る</a>
</div>
