---
layout: default
title: ホーム
---
<header class="tc pv4 bg-white shadow-4 mb3 br3">
  <h1 class="f2 fw9 black">ワンライフ・ナビ</h1>
</header>

<div class="ph2">
  <h2 class="f4 fw6 mb3 bb b--black-10 pb2">カテゴリーから探す</h2>
  <div class="flex flex-wrap">
    {% assign cats = "犬種図鑑,しつけ,食事,健康・医療,お手入れ,お出かけ,年齢診断,その他,FAQ" | split: "," %}
    {% assign icons = "📖,🎾,🍖,🏥,🚿,🚗,🐕,✨,❓" | split: "," %}
    
    {% for cat in cats %}
    <div class="w-50 w-33-ns pa2">
      {% if cat == "犬種図鑑" %}
        {% assign link = '/posts/' %}
      {% elsif cat == "年齢診断" or cat == "食事" or cat == "健康・医療" %}
        {% assign link = '/health-check/' %}
      {% elsif cat == "しつけ" %}
        {% assign link = '/categories/しつけ/' %}
      {% else %}
        {% assign link = '#' %}
      {% endif %}
      
      <a href="{{ link | relative_url }}" class="db ba br3 b--black-10 pa3 bg-white shadow-4 tc no-underline h-100 flex flex-column justify-center hover-bg-gold">
        <span class="f2 db mb2">{{ icons[forloop.index0] }}</span>
        <h2 class="f7 black ma0 fw6">{{ cat }}</h2>
      </a>
    </div>
    {% endfor %}
  </div>
</div>
