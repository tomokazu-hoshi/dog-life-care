---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---

<style>
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { display: none !important; }

  .custom-header { background: white; padding: 15px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  .section-title { text-align: center; font-size: 18px; font-weight: bold; margin: 25px 0 15px; color: #333; }

  .container { padding: 0 15px 40px; }
  .list-card { 
    display: flex; 
    align-items: center; 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.08); 
    margin-bottom: 12px; 
    padding: 15px 20px; 
    text-decoration: none; 
    color: #333;
  }
  .card-icon { font-size: 24px; margin-right: 15px; width: 30px; text-align: center; }
  .card-text { font-size: 15px; font-weight: bold; flex: 1; }
  .card-arrow { color: orange; font-weight: bold; }
</style>

<div class="custom-header">
  <span class="custom-logo">🐶</span>
  <div class="custom-title">ワンライフ・ナビ</div>
</div>

<div class="section-title">犬種図鑑・グループ検索</div>

<div class="container">
  <a href="{{ '/Search-50on/' | relative_url }}" class="list-card">
    <span class="card-icon">🔤</span><span class="card-text">50音検索</span><span class="card-arrow">▶</span>
  </a>
  <a href="{{ '/list/?cat=牧羊犬・牧畜犬' | relative_url }}" class="list-card"><span class="card-icon">🐑</span><span class="card-text">牧羊犬・牧畜犬</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=使役犬' | relative_url }}" class="list-card"><span class="card-icon">🛡️</span><span class="card-text">使役犬</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=テリア' | relative_url }}" class="list-card"><span class="card-icon">🐀</span><span class="card-text">テリア</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=ダックスフンド' | relative_url }}" class="list-card"><span class="card-icon">🌭</span><span class="card-text">ダックスフンド</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=原始的な犬・スピッツ' | relative_url }}" class="list-card"><span class="card-icon">🐕</span><span class="card-text">原始的な犬・スピッツ</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=嗅覚ハウンド' | relative_url }}" class="list-card"><span class="card-icon">👃</span><span class="card-text">嗅覚ハウンド</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=ポインター・セター' | relative_url }}" class="list-card"><span class="card-icon">🏹</span><span class="card-text">ポインター・セター</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=鳥猟犬' | relative_url }}" class="list-card"><span class="card-icon">🦆</span><span class="card-text">鳥猟犬（回収・追い出し）</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=愛玩犬' | relative_url }}" class="list-card"><span class="card-icon">🎀</span><span class="card-text">愛玩犬</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=視覚ハウンド' | relative_url }}" class="list-card"><span class="card-icon">🏎️</span><span class="card-text">視覚ハウンド</span><span class="card-arrow">▶</span></a>
  <a href="{{ '/list/?cat=その他' | relative_url }}" class="list-card"><span class="card-icon">📦</span><span class="card-text">その他</span><span class="card-arrow">▶</span></a>
</div>

<div style="text-align: center; padding-bottom: 40px;">
  <a href="{{ '/' | relative_url }}" style="color: #888; text-decoration: none;">← ホームに戻る</a>
</div>
