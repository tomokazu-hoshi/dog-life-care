---
layout: default
title: 50音検索
permalink: /Search-50on/
---

<style>
  /* 上記 dog-search.md と同じスタイルを適用 */
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  header.site-header, .site-header, .page-title, h1:first-of-type { display: none !important; }
  .custom-header { background: white; padding: 15px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }
  .section-title { text-align: center; font-size: 18px; font-weight: bold; margin: 25px 0 15px; color: #333; }
  .container { padding: 0 15px 40px; }
  .list-card { display: flex; align-items: center; background: white; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.08); margin-bottom: 10px; padding: 15px 20px; text-decoration: none; color: #333; }
  .card-text { font-size: 16px; font-weight: bold; flex: 1; text-align: center; }
  .card-arrow { color: orange; }
</style>

<div class="custom-header">
  <span class="custom-logo">🔤</span>
  <div class="custom-title">50音検索</div>
</div>

<div class="section-title">行を選んでください</div>

<div class="container">
  {% assign lines = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
  {% for line in lines %}
    <a href="{{ '/list/?cat=' | append: line | relative_url }}" class="list-card">
      <span class="card-text">{{ line }}</span>
      <span class="card-arrow">▶</span>
    </a>
  {% endfor %}
</div>

<div style="text-align: center; padding-bottom: 40px;">
  <a href="{{ '/dog-search/' | relative_url }}" style="color: #888; font-size: 14px; text-decoration: none;">← 検索に戻る</a>
</div>
