---
layout: default
title: 健康・医療に関する記事一覧
---

# 🏥 健康・医療
日々の体調チェックや、病気の予防、医療に関する専門的なアドバイス。

<ul>
  {% for post in site.categories.健康・医療 %}
    <li>
      <span style="color: #888;">{{ post.date | date: "%Y.%m.%d" }}</span><br>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<p><a href="/">← トップページへ戻る</a></p>
