---
layout: default
title: 50音検索
permalink: /search-50on/
---
{% include breadcrumb.html %}

<style>
/* 1・2ページ目と統一したデザイン */
.search-header {
  text-align: center;
  padding: 20px 0;
  background: #fff;
}
.search-header h1 { font-size: 1.4rem; color: #333; margin: 0; }

.search-grid {
  display: grid;
  grid-template-columns: 1fr 1fr; /* iPhoneで押しやすい2列配置 */
  gap: 12px;
  padding: 15px;
}
.search-card {
  background: #ffffff;
  border: 1px solid #eee;
  border-radius: 12px;
  padding: 20px 10px;
  text-align: center;
  text-decoration: none;
  color: #333;
  font-weight: bold;
  font-size: 1.1rem;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}
.search-card:active { background: #f9f9f9; transform: scale(0.96); }
</style>

<div class="search-header">
  <h1>50音から探す</h1>
  <p style="font-size: 0.8rem; color: #888; margin-top: 5px;">犬種名の最初の文字を選んでください</p>
</div>

<div class="search-grid">
  <a href="/あ行/" class="search-card">あ行</a>
  <a href="/か行/" class="search-card">か行</a>
  <a href="/さ行/" class="search-card">さ行</a>
  <a href="/た行/" class="search-card">た行</a>
  <a href="/な行/" class="search-card">な行</a>
  <a href="/は行/" class="search-card">は行</a>
  <a href="/ま行/" class="search-card">ま行</a>
  <a href="/や行/" class="search-card">や行</a>
  <a href="/ら行/" class="search-card">ら行</a>
  <a href="/わ行/" class="search-card">わ行</a>
</div>

<div style="text-align: center; margin-top: 30px; padding-bottom: 40px;">
  <a href="/dog-search/" style="color: #888; text-decoration: none; font-size: 0.9rem;">← 犬種図鑑に戻る</a>
</div>
