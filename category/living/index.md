---
layout: default
title: 住まい・環境に関する記事一覧
---

# 🏠 住まい・環境
室内での安全対策や、愛犬がリラックスできる空間づくりの工夫。

<ul>
  {% for post in site.categories.住まい・環境 %}
    <li>
      <span style="color: #888;">{{ post.date | date: "%Y.%m.%d" }}</span><br>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<p><a href="/">← トップページへ戻る</a></p>
