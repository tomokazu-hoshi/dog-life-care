---
layout: default
title: 犬種一覧
permalink: /list/
---

<header class="tc pv3">
  <h1 id="category-title" class="f3 fw9">犬種リスト</h1>
  <p class="f7 gray">記事をタップして詳しく見る</p>
</header>

<div id="breed-list" class="ph2">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="breed-item flex items-center no-underline black bg-white br2 pa3 shadow-2 mb2 dim" style="display:none;" data-cat="{{ post.categories | join: ',' }}">
      <span class="f4 mr3">🐶</span>
      <span class="f6 fw6 flex-auto">{{ post.title }}</span>
      <span class="gold">▶</span>
    </a>
  {% endfor %}
</div>

<script>
  // URLから「どのカテゴリーか」を読み取って、該当する犬種だけを表示する
  const urlParams = new URLSearchParams(window.location.search);
  const selectedCat = urlParams.get('cat');
  
  if (selectedCat) {
    document.getElementById('category-title').innerText = selectedCat;
    const items = document.querySelectorAll('.breed-item');
    items.forEach(item => {
      if (item.getAttribute('data-cat').includes(selectedCat)) {
        item.style.display = 'flex';
      }
    });
  }
</script>

<div class="tc pv4">
  <a href="{{ '/dog-search/' | relative_url }}" class="f7 gray">← 検索に戻る</a>
</div>
