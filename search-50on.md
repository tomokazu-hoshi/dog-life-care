---
layout: default
title: 50音検索
permalink: /Search-50on/
---

<style>
  /* 1. 不要なタイトルを消す */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  
  /* 2. ヘッダー（下線を消し、文字を黒に変更） */
  .custom-header { 
    background: white; padding: 18px 0; text-align: center; 
    display: flex; align-items: center; justify-content: center;
    /* border-bottomを削除しました */
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: #333; margin: 0; } /* 色を黒系に変更 */

  /* 3. 【2列 × 5行】のグリッドレイアウト */
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(2, 1fr); /* 2列にする */
    gap: 15px; /* ボタン同士の隙間 */
    padding: 30px 20px 50px; /* 上部に余白を追加 */
    max-width: 400px; 
    margin: 0 auto; /* 画面中央に寄せる */
  }

  .grid-card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); 
    padding: 25px 10px; /* 縦長で押しやすく */
    text-decoration: none; 
    color: #333; 
    text-align: center; 
    font-size: 20px; /* 文字を大きく */
    font-weight: bold;
    border: 1px solid #eee;
  }
  
  .grid-card:active { background-color: #fff9f0; transform: scale(0.95); } /* 押した時に凹む演出 */

</style>

<div class="custom-header">
  <span class="custom-logo">🔤</span>
  <div class="custom-title">50音検索</div>
</div>

<!-- 「行を選んでください」のテキストを削除しました -->

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
