---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---
{% include breadcrumb.html %}

<style>
.sub-header {
  text-align: center;
  padding: 20px 0;
  background: #fff;
}
.sub-header h1 { font-size: 1.4rem; color: #333; margin: 0; }

.sub-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
  padding: 15px;
}
.sub-card {
  background: #fff;
  border: 1px solid #eee;
  border-radius: 12px;
  padding: 16px 20px;
  text-decoration: none;
  color: #333;
  font-weight: bold;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}
.sub-card:active { background: #f0f0f0; }
/* 50音検索を目立たせる */
.search-50-card {
  background: #e7f5ff;
  border-color: #a5d8ff;
  margin-bottom: 5px;
}
</style>

<div class="sub-header">
  <h1>犬種図鑑</h1>
</div>

<div class="sub-grid">
  <a href="/search-50on/" class="sub-card search-50-card">
    <span>🔍 50音検索（あ、か、さ...）</span>
    <span>＞</span>
  </a>

  <a href="/categories/牧羊犬・牧畜犬/" class="sub-card"><span>牧羊犬・牧畜犬</span><span>＞</span></a>
  <a href="/categories/使役犬/" class="sub-card"><span>使役犬</span><span>＞</span></a>
  <a href="/categories/テリア/" class="sub-card"><span>テリア</span><span>＞</span></a>
  <a href="/categories/ダックスフンド/" class="sub-card"><span>ダックスフンド</span><span>＞</span></a>
  <a href="/categories/原始的な犬・スピッツ/" class="sub-card"><span>原始的な犬・スピッツ</span><span>＞</span></a>
  <a href="/categories/嗅覚ハウンド/" class="sub-card"><span>嗅覚ハウンド</span><span>＞</span></a>
  <a href="/categories/ポインター・セター/" class="sub-card"><span>ポインター・セター</span><span>＞</span></a>
  
  <a href="/categories/鳥猟犬/" class="sub-card">
    <span>鳥猟犬（回収・追い出し）</span>
    <span>＞</span>
  </a>

  <a href="/categories/愛玩犬/" class="sub-card"><span>愛玩犬</span><span>＞</span></a>
  <a href="/categories/視覚ハウンド/" class="sub-card"><span>視覚ハウンド</span><span>＞</span></a>
  <a href="/categories/その他/" class="sub-card"><span>その他</span><span>＞</span></a>
</div>

<div style="text-align: center; margin-top: 20px; padding-bottom: 40px;">
  <a href="/" style="color: #888; text-decoration: none; font-size: 0.9rem;">← ホームに戻る</a>
</div>
