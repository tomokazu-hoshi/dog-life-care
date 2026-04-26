---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---

<style>
  body { font-family: -apple-system, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  .custom-header { background: white; padding: 15px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; }
  .container { padding: 20px 15px; }
  .list-card { display: flex; align-items: center; background: white; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.08); margin-bottom: 12px; padding: 15px 20px; text-decoration: none; color: #333; }
  .card-text { font-size: 15px; font-weight: bold; flex: 1; }
  .card-arrow { color: orange; font-weight: bold; }
</style>

<div class="custom-header">
  <div class="custom-title">🐶 犬種図鑑</div>
</div>

<div class="container">
  <a href="{{ '/Search-50on/' | relative_url }}" class="list-card">
    <span style="font-size: 24px; margin-right: 15px;">🔤</span>
    <span class="card-text">50音検索</span>
    <span class="card-arrow">▶</span>
  </a>

  <a href="{{ '/list/?cat=視覚ハウンド' | relative_url }}" class="list-card">
    <span style="font-size: 24px; margin-right: 15px;">🏎️</span>
    <span class="card-text">視覚ハウンド</span>
    <span class="card-arrow">▶</span>
  </a>
</div>
