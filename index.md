---
layout: default
title: ワンライフ・ナビ
---

<style>
  /* 全体のリセットと背景 */
  body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; background-color: #f6f8fa; color: #333; margin: 0; padding: 0; }
  
  /* 1. ヘッダー：白背景にオレンジのロゴとタイトル */
  .site-custom-header {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: white;
    padding: 18px 0;
    border-bottom: 2px solid #ffcc00;
  }
  .site-logo-icon { font-size: 24px; margin-right: 8px; }
  .site-title-text { font-size: 22px; font-weight: bold; color: #e69500; }

  /* 2. メインビジュアル：愛犬の写真セクション */
  .hero-container {
    position: relative;
    width: 100%;
    line-height: 0;
  }
  .hero-image {
    width: 100%;
    height: auto;
    display: block;
  }
  /* 写真の上の文字（画像のデザインを再現） */
  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0,0,0,0.2); /* 写真を見えやすくしつつ文字を際立たせる */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
    padding: 0 20px;
    line-height: 1.4;
  }
  .hero-headline { font-size: 26px; font-weight: 900; margin-bottom: 10px; text-shadow: 1px 1px 4px rgba(0,0,0,0.6); }
  .hero-subheadline { font-size: 13px; font-weight: 500; text-shadow: 1px 1px 3px rgba(0,0,0,0.6); }

  /* 3. カテゴリーセクション */
  .section-title { text-align: center; font-size: 20px; font-weight: bold; margin: 35px 0 20px; position: relative; padding-bottom: 10px; }
  .section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 40px; height: 3px; background-color: orange; }

  /* グリッドレイアウト */
  .category-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; max-width: 360px; margin: 0 auto; padding: 0 10px 40px; }
  .category-card { background: white; border-radius: 12px; box-shadow: 0 4px 8px rgba(0,0,0,0.08); text-align: center; padding: 15px 5px; text-decoration: none; color: #333; }
  .card-icon { font-size: 30px; margin-bottom: 5px; display: block; }
  .card-label { font-size: 12px; font-weight: bold; }
</style>

<div class="site-custom-header">
  <span class="site-logo-icon">🐾</span>
  <span class="site-title-text">ワンライフ・ナビ</span>
</div>

<div class="hero-container">
  <img src="{{ '/My-dog.PNG' | relative_url }}" class="hero-image" alt="愛犬の写真">
  <div class="hero-overlay">
    <div class="hero-headline">愛犬との時間を、<br>もっと最高に。</div>
    <div class="hero-subheadline">元野犬・雑種の個性を尊重し、共に歩む飼い主さんのための専門ガイド</div>
  </div>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="category-grid">
  <a href="{{ '/training/' | relative_url }}" class="category-card"><span class="card-icon">🎓</span><span class="card-label">しつけ</span></a>
  <a href="{{ '/diet/' | relative_url }}" class="category-card"><span class="card-icon">🍴</span><span class="card-label">食事</span></a>
  <a href="{{ '/health/' | relative_url }}" class="category-card"><span class="card-icon">🩺</span><span class="card-label">健康・医療</span></a>
  <a href="{{ '/care/' | relative_url }}" class="category-card"><span class="card-icon">🚿</span><span class="card-label">お手入れ</span></a>
  <a href="{{ '/dog-search/' | relative_url }}" class="category-card"><span class="card-icon">📖</span><span class="card-label">犬種図鑑</span></a>
  <a href="{{ '/faq/' | relative_url }}" class="category-card"><span class="card-icon">💬</span><span class="card-label">FAQ</span></a>
  <a href="{{ '/outing/' | relative_url }}" class="category-card"><span class="card-icon">🐾</span><span class="card-label">お出かけ</span></a>
  <a href="{{ '/health-check/' | relative_url }}" class="category-card"><span class="card-icon">⌛</span><span class="card-label">年齢診断</span></a>
  <a href="{{ '/others/' | relative_url }}" class="category-card"><span class="card-icon">➕</span><span class="card-label">その他</span></a>
</div>
