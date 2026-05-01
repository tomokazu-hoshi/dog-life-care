---
layout: default
title: 50音検索
permalink: /Search-50on/
---

<style>
  /* 1. テーマ独自のヘッダーや枠線を徹底的に消す */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child, .post-header { 
    display: none !important; 
  }

  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  
  /* 2. カスタムヘッダー（線や影を完全に無効化） */
  .custom-header { 
    background: white !important; 
    padding: 25px 0 !important; 
    text-align: center !important; 
    display: flex !important; 
    align-items: center !important; 
    justify-content: center !important;
    border: none !important;           /* 線を消す */
    border-bottom: none !important;    /* 下線を消す */
    box-shadow: none !important;       /* 影を消す */
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: #333 !important; margin: 0; } 

  /* 3. グリッドレイアウト */
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(2, 1fr); 
    gap: 15px; 
    padding: 20px 20px 50px; 
    max-width: 400px; 
    margin: 0 auto; 
  }

  .grid-card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); 
    padding: 25px 10px; 
    text-decoration: none; 
    color: #333; 
    text-align: center; 
    font-size: 20px; 
    font-weight: bold;
    border: 1px solid #eee;
  }
  
  .grid-card:active { background-color: #fff9f0; transform: scale(0.95); }

</style>

<div class="custom-header">
  <span class="custom-logo">🔤</span>
  <div class="custom-title">50音検索</div>
</div>

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
