---
layout: default
title: ワンライフ・ナビ
---

<style>
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { display: none !important; }
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  .custom-header { background: white; padding: 20px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-logo { font-size: 28px; color: orange; margin-right: 12px; }
  .custom-title { font-size: 26px; font-weight: bold; color: orange; margin: 0; }
  .hero { position: relative; width: 100%; overflow: hidden; background-color: #f0f0f0; min-height: 200px; }
  .hero-img { width: 100%; height: auto; display: block; }
  .hero-text { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; text-align: center; color: white; text-shadow: 2px 2px 10px rgba(0,0,0,0.9); }
  .h-main { font-size: 26px; font-weight: 900; margin-bottom: 12px; line-height: 1.2; }
  .h-sub { font-size: 14px; font-weight: bold; padding: 0 20px; line-height: 1.6; }
  .section-title { text-align: center; font-size: 20px; font-weight: bold; margin: 35px 0 20px; position: relative; padding-bottom: 12px; color: #333; }
  .section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 45px; height: 3px; background-color: orange; border-radius: 2px; }
  .grid-container { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; padding: 0 15px 15px; max-width: 400px; margin: 0 auto; }
  .grid-card { background: white; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); padding: 22px 10px; text-decoration: none; color: #333; display: flex; flex-direction: column; align-items: center; justify-content: center; border: 1px solid #eee; }
  .card-icon { font-size: 32px; margin-bottom: 8px; }
  .card-label { font-size: 13px; font-weight: bold; text-align: center; }
  .wide-button-container { padding: 0 15px 60px; max-width: 400px; margin: 0 auto; }
  .wide-card { background: linear-gradient(135deg, #ff9d00, #ffbb00); border-radius: 15px; box-shadow: 0 4px 15px rgba(255,157,0,0.3); padding: 25px 15px; text-decoration: none; color: white; display: flex; align-items: center; justify-content: center; font-weight: bold; font-size: 17px; text-align: center; }
</style>

<div class="custom-header">
  <span class="custom-logo">🐶</span>
  <div class="custom-title">ワンライフ・ナビ</div>
</div>

<div class="hero">
  <img src="{{ '/my-dog.PNG' | relative_url }}" class="hero-img">
  <div class="hero-text">
    <div class="h-main">愛犬との時間を、<br>もっと最高に。</div>
    <div class="h-sub">愛犬との生活を、より豊かで健康に。<br>飼い主さんと愛犬の幸せを応援する総合ガイド</div>
  </div>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="grid-container">
  <a href="{{ '/training/' | relative_url }}" class="grid-card"><span class="card-icon">🎓</span><span class="card-label">しつけ</span></a>
  <a href="{{ '/outing/' | relative_url }}" class="grid-card"><span class="card-icon">🐾</span><span class="card-label">お出かけ</span></a>
  <a href="{{ '/health/' | relative_url }}" class="grid-card"><span class="card-icon">🩺</span><span class="card-label">健康・医療</span></a>
  <a href="{{ '/care/' | relative_url }}" class="grid-card"><span class="card-icon">🚿</span><span class="card-label">お手入れ</span></a>
  <a href="{{ '/diet/' | relative_url }}" class="grid-card"><span class="card-icon">🍴</span><span class="card-label">食事</span></a>
  <a href="{{ '/health-check/' | relative_url }}" class="grid-card"><span class="card-icon">⌛</span><span class="card-label">年齢シュミレーター</span></a>
  <a href="{{ '/dog-search/' | relative_url }}" class="grid-card"><span class="card-icon">📖</span><span class="card-label">犬種図鑑</span></a>
  <a href="{{ '/faq/' | relative_url }}" class="grid-card"><span class="card-icon">💬</span><span class="card-label">FAQ</span></a>
</div>

<div class="wide-button-container">
  <a href="{{ '/beginners-guide/' | relative_url }}" class="wide-card">
    🔰 初めてワンちゃんを迎えられる方へ
  </a>
</div>
