---
layout: default
title: 50音検索
---
{% include breadcrumb.html %}

<header class="tc pv3">
  <h1 class="f3 fw9 black">50音から探す</h1>
</header>

<div class="ph2">
  <p class="tc gray f7">準備中：あいうえお順で犬種を表示します</p>
  
  <div class="mw7 center">
    {% assign all_posts = site.posts | sort: "title" %}
    {% for post in all_posts %}
    <div class="w-100 mb2">
      <a href="{{ post.url | relative_url }}" class="db ba br2 b--black-10 pa3 bg-white shadow-4 no-underline black flex items-center justify-between">
        <span class="fw6">{{ post.title }}</span>
        <span class="gray f7">＞</span>
      </a>
    </div>
    {% endfor %}
  </div>
</div>

<div class="tc pv4">
  <a href="{{ '/posts/' | relative_url }}" class="f7 gray">← 検索ページに戻る</a>
</div>
