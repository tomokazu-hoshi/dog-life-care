---
layout: default
title: 50音検索
permalink: /Search-50on/
---

<header class="tc pv3">
  <h1 class="f3 fw9">🔤 50音検索</h1>
  <p class="f7 gray">行を選んでください</p>
</header>

<div class="ph2">
  {% assign lines = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
  {% for line in lines %}
    <a href="{{ '/list/?cat=' | append: line | relative_url }}" class="flex items-center no-underline black bg-white br2 pa3 shadow-2 mb2 dim">
      <span class="f5 fw6 flex-auto tc">{{ line }}</span>
      <span class="silver">▶</span>
    </a>
  {% endfor %}
</div>

<div class="tc pv4">
  <a href="{{ '/dog-search/' | relative_url }}" class="f7 gray">← 検索に戻る</a>
</div>
