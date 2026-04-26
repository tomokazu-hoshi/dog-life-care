---
layout: default
title: ワンライフ・ナビ
---

<style>
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  .site-header { display: none; } /* テーマ独自のヘッダーを消す */
  
  /* 1. ヘッダー */
  .custom-header { background: white; padding: 15px 0; text-align: center; border-bottom: 3px solid orange; }
  .custom-title { font-size: 24px; font-weight: bold; color: orange; margin: 0; }

  /* 2. 写真エリア */
  .hero { position: relative; width: 100%; overflow: hidden; background-color: #eee; }
  .hero-img { width: 100%; height: auto; display: block; }
  
  /* 写真の上のキャッチコピー（文字） */
  .hero-text { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; text-align: center; color: white; text-shadow: 2px 2px 4px rgba(0,0,0,0.7); }
  .h-main { font-size: 26px; font-weight: 900; margin-bottom: 10px; }
  .h-sub { font-size: 13px; font-weight: bold; padding: 0 20px; line-height: 1.5; }

  /* 3. カテゴリー */
  .section-title { text-align: center; font-size: 20px; font-weight: bold; margin: 30px 0 20px; position: relative; padding-bottom: 10px; }
  .section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 40px; height: 3px; background-color: orange; }

  .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; max-width: 360px; margin: 0 auto; padding: 0 10px 50px; }
  .card { background: white; border-radius: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); text-align: center; padding: 15px 5px; text-decoration: none; color: #333; display: flex; flex-direction: column; justify-content: center; align-items: center; min-height: 80px; }
  .card-icon { font-size: 32px; }
  .card-label { font-size: 12px; font-weight: bold; margin-top: 5px; }
</style>

<div class="custom-header">
  <div class="custom-title">ワンライフナビ</div>
</div>

<div class="hero">
  <img src="{{ '/My-dog.PNG' | relative_url }}" class="hero-img" alt="" title="">
  <div class="hero-text">
    <div class="h-main">愛犬との時間を、<br>もっと最高に。</div>
    <div class="h-sub">元野犬・雑種の個性を尊重し、共に歩む飼い主さんのための専門ガイド</div>
  </div>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="grid">
  <a href="{{ '/training/' | relative_url }}" class="card"><span class="card-icon">🎓</span><span class="card-label">しつけ</span></a>
  <a href="{{ '/diet/' | relative_url }}" class="card"><span class="card-icon">🍴</span><span class="card-label">食事</span></a>
  <a href="{{ '/health/' | relative_url }}" class="card"><span class="card-icon">🩺</span><span class="card-label">健康・医療</span></a>
  <a href="{{ '/care/' | relative_url }}" class="card"><span class="card-icon">🚿</span><span class="card-label">お手入れ</span></a>
  
  <a href="{{ '/dog-search/' | relative_url }}" class="card"><span class="card-icon">📖</span></a>
  
  <a href="{{ '/faq/' | relative_url }}" class="card"><span class="card-icon">💬</span><span class="card-label">FAQ</span></a>
  <a href="{{ '/outing/' | relative_url }}" class="card"><span class="card-icon">🐾</span><span class="card-label">お出かけ</span></a>
  <a href="{{ '/health-check/' | relative_url }}" class="card"><span class="card-icon">⌛</span><span class="card-label">年齢診断</span></a>
  <a href="{{ '/others/' | relative_url }}" class="card"><span class="card-icon">➕</span><span class="card-label">その他</span></a>
</div>
