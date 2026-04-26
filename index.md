---
layout: default
title: ワンライフ・ナビ
---

<style>
  /* --- GLOBAL THEME OVERRIDES --- */
  /* Jekyllのテーマ Primerの枠を homepage（index.md）だけ完全にオーバーライドするためのCSS */
  body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; background-color: #f6f8fa; color: #333; margin: 0; padding: 0; }
  .homepage-body-container { margin: 0; padding: 0; } /* We will put everything in this */
  .site-header { display: none; } /* デフォルトのPrimerテーマヘッダーを消す */
  .main-content { padding: 0; } /* デフォルトのPrimersコンテナのパディングを消す */

  /* --- NEW CUSTOM HEADER (SITE TITLE) --- */
  /* 画像3.png：白背景にオレンジのロゴとタイトル */
  .site-custom-header {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: white;
    padding: 18px 0;
    border-bottom: 3px solid orange; /* テーマのオレンジライン */
  }
  .site-logo-icon {
    font-size: 30px;
    color: orange;
    margin-right: 12px;
  }
  .site-title-text {
    font-size: 26px;
    font-weight: bold;
    color: orange; /* サイトタイトルをオレンジ色に */
  }

  /* --- NEW HERO PHOTO SECTION (YOUR DOG PHOTO) --- */
  /* 画像3.png：大きな犬の写真とその上のテキスト */
  .hero-photo-section {
    position: relative;
    width: 100%;
    /* Primerテーマのコンテナから飛び出すための魔法のCSS (iPhone用) */
    margin-left: calc(-50vw + 50%);
    margin-right: calc(-50vw + 50%);
    width: 100vw;
    overflow: hidden;
    margin-bottom: 0;
  }
  
  /* 写真をここに置いてください：灰色のプレースホルダー（まだ写真がない時用） */
  .hero-image-placeholder {
    width: 100%;
    height: auto;
    display: block;
    background-color: #ddd; /* 灰色のスペース */
    min-height: 250px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #777;
    font-weight: bold;
    text-align: center;
    padding: 20px;
  }
  /* あなたの写真がアップロードされた時に適用されるCSS */
  .hero-image {
    width: 100%;
    height: auto;
    display: block;
    /* 暂定的にPlaceholderと同じCSSを割り当て。Placeholderを消して、<img>タグを使う */
  }

  /* 写真の上のテキストオーバーレイ（画像3.png） */
  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background-color: rgba(0,0,0,0.3); /* 文字を読みやすくするための暗いオーバーレイ */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
    padding: 0 15px;
  }
  .hero-headline {
    font-size: 28px;
    font-weight: 900;
    line-height: 1.2;
    margin-bottom: 12px;
  }
  .hero-subheadline {
    font-size: 14px;
    line-height: 1.6;
    max-width: 320px;
    margin: 0 auto;
  }

  /* --- PREVIOUS SECTION: SECTION TITLE & CATEGORY GRID --- */
  /* セクションタイトル：オレンジ下線付き */
  .custom-section-title { text-align: center; font-size: 24px; font-weight: bold; margin-top: 45px; margin-bottom: 30px; position: relative; padding-bottom: 14px; color: #333; }
  .custom-section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 45px; height: 3px; background-color: orange; border-radius: 2px; }

  /* 3x3 グリッドレイアウト（iPhone用） */
  .custom-category-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; max-width: 360px; margin: 0 auto; padding: 0 10px; margin-bottom: 50px; }

  /* カテゴリーカード（リンク）：白背景、角丸、シャドウ（画像4.png） */
  .custom-category-card { background-color: white; border-radius: 12px; box-shadow: 0 3px 6px rgba(0,0,0,0.1); text-align: center; padding: 20px 5px; text-decoration: none; color: #333; display: flex; flex-direction: column; align-items: center; }
  
  /* カード内のアイコン */
  .custom-card-icon { width: 45px; height: 45px; margin-bottom: 10px; font-size: 36px; color: orange; }
  
  /* カード内のテキスト（「しつけ」など） */
  .custom-card-title { font-size: 14px; font-weight: bold; line-height: 1.2; }
</style>

<div class="site-custom-header homepage-body-container">
  <span class="site-logo-icon">🐶</span> <span class="site-title-text">ワンライフナビ</span> </div>

<div class="hero-photo-section">
  <div class="hero-image-placeholder">
    <div class="hero-overlay">
      <div class="hero-headline">愛犬との時間を、もっと最高に。</div>
      <div class="hero-subheadline">
        元野犬・雑種の個性を尊重し、共に歩む飼い主さんのための専門ガイド
      </div>
    </div>
  </div>
</div>

<div class="custom-section-titlehomepage-body-container">カテゴリーから探す</div>

<div class="custom-category-grid">
  <a href="{{ '/training/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🎓</div>
    <div class="custom-card-title">しつけ</div>
  </a>
  <a href="{{ '/diet/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🍴</div>
    <div class="custom-card-title">食事</div>
  </a>
  <a href="{{ '/health/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🩺</div>
    <div class="custom-card-title">健康・医療</div>
  </a>
  <a href="{{ '/care/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🚿</div>
    <div class="custom-card-title">お手入れ</div>
  </a>
  <a href="{{ '/dog-search/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">📖</div>
    <div class="custom-card-title">犬種図鑑</div>
  </a>
  <a href="{{ '/faq/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">💬</div>
    <div class="custom-card-title">FAQ</div>
  </a>
  <a href="{{ '/outing/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🐾</div>
    <div class="custom-card-title">お出かけ</div>
  </a>
  <a href="{{ '/health-check/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">⌛</div>
    <div class="custom-card-title">年齢診断</div>
  </a>
  <a href="{{ '/others/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">➕</div>
    <div class="custom-card-title">その他</div>
  </a>
</div>
