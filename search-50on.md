---
layout: default
title: 50音検索
permalink: /search-50on/
---
{% include breadcrumb.html %}

<header style="text-align: center; padding: 20px 0;">
  <h1 style="font-size: 1.5rem; font-weight: bold; color: #333;">50音から探す</h1>
</header>

<div style="padding: 0 10px;">
  <div style="display: flex; flex-wrap: wrap; margin: 0 -5px;">
    {% assign rows = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
    {% for row in rows %}
    <div style="width: 50%; padding: 5px; box-sizing: border-box;">
      <a href="/{{ row }}/" style="display: flex; align-items: center; justify-content: center; height: 80px; background: white; border: 1px solid #ddd; border-radius: 12px; text-decoration: none; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
        <h2 style="font-size: 1.2rem; color: #333; margin: 0;">{{ row }}</h2>
      </a>
    </div>
    {% endfor %}
  </div>
</div>

<div style="text-align: center; padding: 30px 0;">
  <a href="/" style="font-size: 0.9rem; color: #888; text-decoration: none;">← トップページに戻る</a>
</div>
