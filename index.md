---
layout: default
title: ワンライフ・ナビ | ホーム
---

<style>
/* iPhone専用：押しやすく清潔感のあるタイルデザイン */
.main-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  padding: 15px;
}
.main-card {
  background: #ffffff;
  border: 1px solid #eee;
  border-radius: 16px;
  padding: 20px 10px;
  text-align: center;
  text-decoration: none;
  color: #333;
  box-shadow: 0 4px 10px rgba(0,0,0,0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
}
.main-card:active { transform: scale(0.96); background: #f9f9f9; }
.card-icon { font-size: 1.8rem; margin-bottom: 8px; }
.card-text { font-weight: bold; font-size: 0.85rem; }

/* 犬種図鑑（2ページ目へ）を一番目立たせる */
.card-special {
  background: #fff9db;
  border-color: #fab005;
  grid-column: span 2;
  padding: 25px 10px;
}
.card-special .card-text { font-size: 1.1rem; }
</style>

<div style="text-align: center; padding: 25px 0 10px;">
  <h1 style="margin: 0; font-size: 1.6rem; color: #333;">ワンライフ・ナビ</h1>
  <p style="font-size: 0.8rem; color: #888; margin-top: 5px;">愛犬との一生を豊かにするガイド</p>
</div>

<div class="main-grid">
  <a href="/dog-search/" class="main-card card-special">
    <span class="card-icon">🐕</span>
    <span class="card-text">犬種図鑑</span>
  </a>

  <a href="/categories/しつけ/" class="main-card">
    <span class="card-icon">🎓</span>
    <span class="card-text">しつけ</span>
  </a>
  <a href="/categories/食事/" class="main-card">
    <span class="card-icon">🍖</span>
    <span class="card-text">食事</span>
  </a>
  <a href="/categories/健康・医療/" class="main-card">
    <span class="card-icon">🏥</span>
    <span class="card-text">健康・医療</span>
  </a>
  <a href="/categories/お手入れ/" class="main-card">
    <span class="card-icon">✂️</span>
    <span class="card-text">お手入れ</span>
  </a>
  <a href="/categories/お出かけ/" class="main-card">
    <span class="card-icon">🚗</span>
    <span class="card-text">お出かけ</span>
  </a>
  <a href="/categories/年齢診断/" class="main-card">
    <span class="card-icon">📅</span>
    <span class="card-text">年齢診断</span>
  </a>
  <a href="/categories/その他/" class="main-card">
    <span class="card-icon">📁</span>
    <span class="card-text">その他</span>
  </a>
  <a href="/categories/FAQ/" class="main-card">
    <span class="card-icon">❓</span>
    <span class="card-text">FAQ</span>
  </a>
</div>
