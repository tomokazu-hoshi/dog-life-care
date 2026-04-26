---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---

# 🐕 犬種図鑑・検索

調べたいカテゴリーをタップすると、該当する犬種が表示されます。

## 🔤 50音検索
<ul>
  {% for post in site.categories["あ行"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
  {% comment %} い、う、え、お等も自動で「あ行」カテゴリーに入っていればここに並びます {% endcomment %}
</ul>

## 🐑 牧羊犬・牧畜犬
<ul>
  {% for post in site.categories["牧羊犬・牧畜犬"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🛡️ 使役犬
<ul>
  {% for post in site.categories["使役犬"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🐀 テリア
<ul>
  {% for post in site.categories["テリア"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🌭 ダックスフンド
<ul>
  {% for post in site.categories["ダックスフンド"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🐕 原始的な犬・スピッツ
<ul>
  {% for post in site.categories["原始的な犬・スピッツ"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 👃 嗅覚ハウンド
<ul>
  {% for post in site.categories["嗅覚ハウンド"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🏹 ポインター・セター
<ul>
  {% for post in site.categories["ポインター・セター"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🦆 鳥猟犬（回収・追い出し）
<ul>
  {% for post in site.tags["鳥猟犬"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
  {% comment %} ここだけは指示通り「タグ」から探すようにしています {% endcomment %}
</ul>

## 🎀 愛玩犬
<ul>
  {% for post in site.categories["愛玩犬"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 🏎️ 視覚ハウンド
<ul>
  {% for post in site.categories["視覚ハウンド"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 📦 その他
<ul>
  {% for post in site.categories["その他"] %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

---
[🏠 ホームに戻る]({{ '/' | relative_url }})
