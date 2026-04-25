---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---
{% include breadcrumb.html %}

<header class="tc pv3">
  <h1 class="f3 fw9 black">犬種図鑑 検索</h1>
</header>

<div class="mb4 ph2">
  <a href="{{ '/search-50on/' | relative_url }}" class="db ba br3 b--black-10 pa4 bg-white shadow-4 tc no-underline hover-bg-gold">
    <h2 class="f4 black ma0">50音検索</h2>
    <p class="f7 gray ma0 mt1">名前から探す</p>
  </a>
</div>

<div class="flex flex-wrap ph1">
  {% assign groups = "牧羊犬・牧畜犬,使役犬,テリア,ダックスフンド,原始的な犬・スピッツ,嗅覚ハウンド,ポインター・セター,鳥猟犬（回収・追い出し）,愛玩犬,視覚ハウンド,その他" | split: "," %}
  {% for group in groups %}
  <div class="w-50 pa2">
    <a href="{{ '/categories/' | append: group | append: '/' | relative_url }}" class="db ba br3 b--black-10 pa3 bg-white shadow-4 tc no-underline h-100 flex items-center justify-center hover-bg-gold">
      <h2 class="f7 black ma0 fw6">{{ group }}</h2>
    </a>
  </div>
  {% endfor %}
</div>
