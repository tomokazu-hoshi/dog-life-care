---
layout: default
title: ワンライフ・ナビ | 愛犬との一生を豊かにするガイド
---

<style>
/* iPhoneでの操作性を重視したスタイル */
.hero {
  background: linear-gradient(135deg, #ff922b, #fab005);
  color: white;
  padding: 40px 20px;
  text-align: center;
  border-radius: 0 0 30px 30px;
  margin: -20px -20px 30px -20px;
}
.hero h1 { margin: 0; font-size: 1.8em; }
.hero p { margin: 10px 0 0; opacity: 0.9; font-size: 0.9em; }

.section-title {
  font-size: 1.2em;
  font-weight: bold;
  margin: 30px 0 15px;
  padding-left: 10px;
  border-left: 4px solid #ff922b;
}

.category-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 15px;
}

.card {
  background: #ffffff;
  border-radius: 15px;
  padding: 20px;
  text-align: center;
  text-decoration: none;
  color: #444;
  box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  transition: transform 0.2s;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.card:active { transform: scale(0.95); }
.card-icon { font-size: 2em; margin-bottom: 10px; }
.card-label { font-weight: bold; font-size: 0.9em; }

.post-list {
  list-style: none;
  padding: 0;
}
.post-item {
  background: #fff;
  margin-bottom: 10px;
  padding: 15px;
  border-radius: 12px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.03);
}
.post-date { font-size: 0.8em; color: #888; }
.post-link { text-decoration: none; color: #333; font-weight: 500; display: block; margin-top: 5px; }

.btn-archive {
  display: block;
  text-align: center;
  background: #f1f3f5;
  color: #495057;
  padding: 12px;
  border-radius: 10px;
  text-decoration: none;
  margin-top: 15px;
  font-size: 0.9em;
}
</style>

<div class="hero">
  <h1>ワンライフ・ナビ</h1>
  <p>愛犬と歩む、最高の「一生」のために。</p>
</div>

<div class="section-title">カテゴリーから探す</div>

<div class="category-grid">
  <a href="/categories/diet/" class="card">
    <span class="card-icon">🍖</span>
    <span class="card-label">食事</span>
  </a>
  <a href="/categories/health/" class="card">
    <span class="card-icon">🏥</span>
    <span class="card-label">健康</span>
  </a>
  <a href="/categories/care/" class="card">
    <span class="card-icon">✂️</span>
    <span class="card-label">お手入れ</span>
  </a>
  <a href="/categories/training/" class="card">
    <span class="card-icon">🎓</span>
    <span class="card-label">しつけ</span>
  </a>
  <a href="/categories/outing/" class="card">
    <span class="card-icon">🚗</span>
    <span class="card-label">お出かけ</span>
  </a>
  <a href="/categories/living/" class="card">
    <span class="card-icon">🏠</span>
    <span class="card-label">住まい</span>
  </a>
  <a href="/search-50on/" class="card" style="grid-column: span 2; background: #fff9db;">
    <span class="card-icon">🐕</span>
    <span class="card-label">犬種図鑑（50音順）で検索する</span>
  </a>
</div>

<div class="section-title">最新のアドバイス</div>

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li class="post-item">
      <div class="post-date">{{ post.date | date: "%Y.%m.%d" }}</div>
      <a href="{{ post.url }}" class="post-link">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<a href="/search-50on/" class="btn-archive">すべての記事・犬種を見る</a>
