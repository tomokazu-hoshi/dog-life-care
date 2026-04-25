---
layout: default
title: 50音検索
permalink: /search-50on/
---
{% include breadcrumb.html %}

<header class="tc pv3">
  <h1 class="f3 fw9 black">50音から探す</h1>
</header>

<div class="ph2">
  <div class="flex flex-wrap ph1">
    {% assign rows = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
    {% for row in rows %}
    <div class="w-50 pa2">
      <a href="{{ '/categories/' | append: row | append: '/' | relative_url }}" class="db ba br3 b--black-10 pa4 bg-white shadow-4 tc no-underline h-100 flex items-center justify-center hover-bg-gold">
        <h2 class="f3 black ma0 fw6">{{ row }}</h2>
      </a>
    </div>
    {% endfor %}
  </div>
</div>

<div class="tc pv4">
  <a href="{{ '/posts/' | relative_url }}" class="f7 gray">← 検索ページに戻る</a>
</div>
