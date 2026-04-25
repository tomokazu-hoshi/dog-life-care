---
layout: default
title: ワンライフ・ナビ | 愛犬との一生を豊かにするナビゲーション
---

# ワンライフ・ナビへようこそ
**愛犬との健やかで幸せな毎日をサポートする情報ガイド**

---

## 🔍 カテゴリーから探す

<div class="category-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 10px;">
  <a href="/category/diet/" style="padding: 15px; background: #fff4e6; text-align: center; border-radius: 10px; text-decoration: none; color: #d9480f; font-weight: bold; font-size: 0.9em;">🍖 食事</a>
  <a href="/category/health/" style="padding: 15px; background: #e7f5ff; text-align: center; border-radius: 10px; text-decoration: none; color: #1971c2; font-weight: bold; font-size: 0.9em;">🏥 健康</a>
  <a href="/category/care/" style="padding: 15px; background: #f3f0ff; text-align: center; border-radius: 10px; text-decoration: none; color: #6741d9; font-weight: bold; font-size: 0.9em;">✂️ お手入れ</a>
  <a href="/category/training/" style="padding: 15px; background: #fff5f5; text-align: center; border-radius: 10px; text-decoration: none; color: #c2255c; font-weight: bold; font-size: 0.9em;">🎓 しつけ</a>
  <a href="/category/outing/" style="padding: 15px; background: #ebfbee; text-align: center; border-radius: 10px; text-decoration: none; color: #2b8a3e; font-weight: bold; font-size: 0.9em;">🚗 外出</a>
  <a href="/category/living/" style="padding: 15px; background: #fff0f6; text-align: center; border-radius: 10px; text-decoration: none; color: #d6336c; font-weight: bold; font-size: 0.9em;">🏠 住まい</a>
  <a href="/search/" style="padding: 15px; background: #fff9db; text-align: center; border-radius: 10px; text-decoration: none; color: #f08c00; font-weight: bold; font-size: 0.9em;">🐕 犬種図鑑</a>
</div>

---

## 🆕 最新の記事
これまでに作成した最新のアドバイスをお届けします。

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <span style="color: #888; font-size: 0.9em;">{{ post.date | date: "%Y.%m.%d" }}</span><br>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<div style="text-align: center; margin-top: 30px;">
  <a href="/archive/" style="display: inline-block; padding: 10px 20px; background: #333; color: #fff; border-radius: 5px; text-decoration: none;">すべての記事を見る</a>
</div>

---

### コンセプト
「ワンライフ・ナビ」は、食事、医療、日常のケア、そして最高の思い出作りまで、飼い主さんが直面するあらゆる疑問に寄り添うメディアを目指しています。
