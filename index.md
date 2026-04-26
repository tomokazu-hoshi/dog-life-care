---
layout: default
title: ワンライフ・ナビ
---

<style>
  /* 1. 【最優先】テーマの不要な文字を強制的に消す命令（これは維持します） */
  header.site-header, 
  .site-header, 
  .page-title, 
  h1:first-of-type, 
  .main-content h1:first-child { 
    display: none !important; 
    visibility: hidden !important; 
    height: 0 !important; 
    margin: 0 !important; 
    padding: 0 !important;
  }

  /* 2. 全体のデザイン設定 */
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  
  /* 3. 新しいオレンジ色のヘッダー（ロゴを追加） */
  .custom-header { 
    background: white; 
    padding: 20px 0; 
    text-align: center; 
    border-bottom: 3px solid orange; 
    display: flex; /* ロゴとタイトルを横並びにする */
    align-items: center;
    justify-content: center;
  }
  .custom-logo {
    font-size: 28px; /* ロゴの大きさ */
    color: orange; /* ロゴの色 */
    margin-right: 12px; /* タイトルとの間隔 */
  }
  .custom-title { 
    font-size: 26px; 
    font-weight: bold; 
    color: orange; 
    margin: 0; 
  }

  /* 4. メイン写真エリア */
  .hero { position: relative; width: 100%; overflow: hidden; background-color: #f0f0f0; min-height: 200px; }
  .hero-img { width: 100%; height: auto; display: block; }
  
  /* 写真の上のテキスト（キャッチコピー） */
  .hero-text { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; text-align: center; color: white; text-shadow: 2px 2px 10px rgba(0,0,0,0.9); }
  .h-main { font-size: 26px; font-weight: 900; margin-bottom: 12px; line-height: 1.2; }
  .h-sub { font-size: 14px; font-weight: bold; padding: 0 20px; line-height: 1.6; }

  /* 5. カテゴリー */
  .section-title { text-align: center; font-size: 20px; font-weight: bold; margin: 35px 0 20px; position: relative; padding-bottom: 12px; color: #333; }
  .section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 45px; height: 3px; background-color: orange; border-radius: 2px; }

  .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; max-width: 360px; margin: 0 auto; padding: 0 10px 60px; }
  .card { background: white; border-radius: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); text-align: center; padding: 18px 5px; text-decoration: none; color: #333; display: flex; flex-direction: column; justify-content: center; align-items: center; min-height: 85px; }
  .card-icon { font-size: 34px; margin-bottom: 4px; }
  .card-label { font-size: 12px; font-weight: bold; }
</style>

<div class="custom-header">
  <span class="custom-logo">🐶</span> <div class="custom-title">ワンライフ・ナビ</div>
</div>

<div class="hero">
  <img src="{{ '/my-dog.PNG' | relative_url }}" class="hero-img" alt="">
  <div class="hero-text">
    <div class="h-main">愛犬との時間を、<br>もっと最高に。</div>
    <div class="h-sub">
      愛犬との生活を、より豊かで健康に。<br>
      飼い主さんと愛犬の幸せを応援する総合ガイド
    </div>
  </div>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="grid">
  <a href="{{ '/training/' | relative_url }}" class="card"><span class="card-icon">🎓</span><span class="card-label">しつけ</span></a>
  <a href="{{ '/diet/' | relative_url }}" class="card"><span class="card-icon">🍴</span><span class="card-label">食事</span></a>
  <a href="{{ '/health/' | relative_url }}" class="card"><span class="card-icon">🩺</span><span class="card-label">健康・医療</span></a>
  <a href="{{ '/care/' | relative_url }}" class="card"><span class="card-icon">🚿</span><span class="card-label">お手入れ</span></a>
  <a href="{{ '/dog-search/' | relative_url }}" class="card"><span class="card-icon">📖</span><span class="card-label">犬種図鑑</span></a>
  <a href="{{ '/faq/' | relative_url }}" class="card"><span class="card-icon">💬</span><span class="card-label">FAQ</span></a>
  <a href="{{ '/outing/' | relative_url }}" class="card"><span class="card-icon">🐾</span><span class="card-label">お出かけ</span></a>
  <a href="{{ '/health-check/' | relative_url }}" class="card"><span class="card-icon">⌛</span><span class="card-label">年齢診断</span></a>
  <a href="{{ '/others/' | relative_url }}" class="card"><span class="card-icon">➕</span><span class="card-label">その他</span></a>
</div>
