---
layout: default
title: 犬種図鑑 検索
permalink: /dog-search/
---

<style>
  /* アコーディオンの三角矢印を消して、ボックスらしくする設定 */
  details summary::-webkit-details-marker { display:none; }
  summary { list-style: none; outline: none; transition: 0.2s; }
  details[open] summary { border-bottom: 1px solid #eee; border-radius: 8px 8px 0 0; }
</style>

<header class="tc pv3">
  <h1 class="f3 fw9">🐕 犬種図鑑 検索</h1>
  <p class="f7 gray">カテゴリーをタップして犬種を探す</p>
</header>

<div class="flex flex-wrap justify-center ph2">

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white hover-bg-near-white">
      <div class="f2 mb1">🔤</div>
      <div class="f6 fw6">50音検索</div>
    </summary>
    <div class="pa3 bg-near-white">
      {% assign lines = "あ行,か行,さ行,た行,な行,は行,ま行,や行,ら行,わ行" | split: "," %}
      {% for line in lines %}
        {% if site.categories[line].size > 0 %}
          <h4 class="f8 fw6 silver mb1 mt2 bb b--moon-gray">{{ line }}</h4>
          <ul class="list pl0 mt0 mb3">
            {% for post in site.categories[line] %}
              <li class="mv1"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
            {% endfor %}
          </ul>
        {% endif %}
      {% endfor %}
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🐑</div>
      <div class="f6 fw6">牧羊犬・牧畜犬</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["牧羊犬・牧畜犬"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🛡️</div>
      <div class="f6 fw6">使役犬</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["使役犬"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🐀</div>
      <div class="f6 fw6">テリア</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["テリア"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🌭</div>
      <div class="f6 fw6">ダックスフンド</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["ダックスフンド"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🐕</div>
      <div class="f6 fw6">原始的な犬・スピッツ</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["原始的な犬・スピッツ"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">👃</div>
      <div class="f6 fw6">嗅覚ハウンド</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["嗅覚ハウンド"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🏹</div>
      <div class="f6 fw6">ポインター・セター</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["ポインター・セター"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🦆</div>
      <div class="f6 fw6">鳥猟犬（回収・追い出し）</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["鳥猟犬"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🎀</div>
      <div class="f6 fw6">愛玩犬</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["愛玩犬"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">🏎️</div>
      <div class="f6 fw6">視覚ハウンド</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["視覚ハウンド"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

  <details class="w-100 ma2 shadow-4 br3 bg-white overflow-hidden">
    <summary class="pa3 tc pointer bg-white">
      <div class="f2 mb1">📦</div>
      <div class="f6 fw6">その他</div>
    </summary>
    <div class="pa3 bg-near-white">
      <ul class="list pl0 ma0">
        {% for post in site.categories["その他"] %}
          <li class="mv2"><a href="{{ post.url | relative_url }}" class="link gold fw6 f6">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  </details>

</div>

<div class="tc pv4">
  <a href="{{ '/' | relative_url }}" class="f7 gray">← ホームに戻る</a>
</div>
