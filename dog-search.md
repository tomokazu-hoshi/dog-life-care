---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---

<style>
  /* 1. 不要なタイトルを強制的に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  
  /* 2. オレンジのヘッダー */
  .custom-header { 
    background: white; padding: 18px 0; text-align: center; border-bottom: 3px solid orange; 
    display: flex; align-items: center; justify-content: center;
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  .section-title { text-align: center; font-size: 18px; font-weight: bold; margin: 25px 0 15px; color: #333; }

  /* 3. 【2列 × 6行】のグリッドレイアウト */
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(2, 1fr); /* 横に2つ並べる */
    gap: 12px; /* ボタン同士の隙間 */
    padding: 0 15px 50px; 
    max-width: 400px; 
    margin: 0 auto; /* 画面中央に配置 */
  }

  .grid-card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); 
    padding: 20px 5px; 
    text-decoration: none; 
    color: #333; 
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid #eee;
  }
  
  .grid-card:active { background-color: #fff9f0; transform: scale(0.95); }

  .card-icon { font-size: 28px; margin-bottom: 8px; }
  .card-text { font-size: 13px; font-weight: bold; text-align: center; line-height: 1.3; }

</style>

<div class="custom-header">
  <span class="custom-logo">🐶</span>
  <div class="custom-title">ワンライフ・ナビ</div>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="grid-container">
  <a href="{{ '/Search-50on/' | relative_url }}" class="grid-card">
    <span class="card-icon">🔤</span>
    <span class="card-text">50音検索</span>
  </a>

  <a href="{{ '/list/?cat=牧羊犬・牧畜犬' | relative_url }}" class="grid-card">
    <span class="card-icon">🐑</span>
    <span class="card-text">牧羊犬・牧畜犬</span>
  </a>

  <a href="{{ '/list/?cat=使役犬' | relative_url }}" class="grid-card">
    <span class="card-icon">🛡️</span>
    <span class="card-text">使役犬</span>
  </a>

  <a href="{{ '/list/?cat=テリア' | relative_url }}" class="grid-card">
    <span class="card-icon">🐀</span>
    <span class="card-text">テリア</span>
  </a>

  <a href="{{ '/list/?cat=ダックスフンド' | relative_url }}" class="grid-card">
    <span class="card-icon">🌭</span>
    <span class="card-text">ダックスフンド</span>
  </a>

  <a href="{{ '/list/?cat=原始的な犬・スピッツ' | relative_url }}" class="grid-card">
    <span class="card-icon">🐕</span>
    <span class="card-text">原始的な犬・スピッツ</span>
  </a>

  <a href="{{ '/list/?cat=嗅覚ハウンド' | relative_url }}" class="grid-card">
    <span class="card-icon">👃</span>
    <span class="card-text">嗅覚ハウンド</span>
  </a>

  <a href="{{ '/list/?cat=ポインター・セター' | relative_url }}" class="grid-card">
    <span class="card-icon">🏹</span>
    <span class="card-text">ポインター・セター</span>
  </a>

  <a href="{{ '/list/?cat=鳥猟犬' | relative_url }}" class="grid-card">
    <span class="card-icon">🦆</span>
    <span class="card-text">鳥猟犬<br>(回収・追い出し)</span>
  </a>

  <a href="{{ '/list/?cat=愛玩犬' | relative_url }}" class="grid-card">
    <span class="card-icon">🎀</span>
    <span class="card-text">愛玩犬</span>
  </a>

  <a href="{{ '/list/?cat=視覚ハウンド' | relative_url }}" class="grid-card">
    <span class="card-icon">🏎️</span>
    <span class="card-text">視覚ハウンド</span>
  </a>

  <a href="{{ '/list/?cat=その他' | relative_url }}" class="grid-card">
    <span class="card-icon">📦</span>
    <span class="card-text">その他</span>
  </a>
</div>

<div style="text-align: center; padding-bottom: 50px;">
  <a href="{{ '/' | relative_url }}" style="color: #888; font-size: 14px; text-decoration: none;">← ホームに戻る</a>
</div>
