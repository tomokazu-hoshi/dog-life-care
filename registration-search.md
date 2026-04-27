---
layout: default
title: 自治体検索
permalink: /registration-search/
---

<style>
  header.site-header, .site-header, .page-title, h1:first-of-type { display: none !important; }
  body { font-family: -apple-system, sans-serif; background: #f6f8fa; padding-bottom: 50px; }

  .search-header { background: white; padding: 20px; text-align: center; border-bottom: 3px solid orange; }
  .search-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }
  
  .container { padding: 15px; }
  .step-title { font-size: 14px; font-weight: bold; color: #666; margin: 15px 0 10px; }

  /* 都道府県ボタン */
  .pref-btn { 
    background: white; border: 1px solid #ddd; border-radius: 10px; padding: 15px; 
    width: 100%; text-align: left; margin-bottom: 10px; font-weight: bold; 
    display: flex; justify-content: space-between; align-items: center;
  }
  .pref-btn::after { content: "▼"; font-size: 10px; color: orange; }

  /* 市町村リスト（最初は隠す） */
  .city-list { 
    display: none; background: #fff9f0; padding: 10px; border-radius: 0 0 10px 10px; 
    margin-top: -10px; margin-bottom: 15px; border: 1px solid #ffd8a8; border-top: none;
  }
  .city-link { 
    display: block; padding: 12px; color: #333; text-decoration: none; 
    border-bottom: 1px solid #ffe8cc; font-size: 14px; 
  }
  .city-link:last-child { border-bottom: none; }
</style>

<div class="search-header">
  <div class="search-title">全国自治体 登録窓口検索</div>
</div>

<div class="container">
  <p style="font-size: 13px; color: #888;">お住まいの都道府県を選択してください。</p>

  <button class="pref-btn" onclick="toggleCity('tokyo')">東京都</button>
  <div id="tokyo" class="city-list">
    <a href="https://www.city.shinjuku.lg.jp/kenkou/yobo01_001004.html" class="city-link">新宿区</a>
    <a href="https://www.city.setagaya.lg.jp/mokuji/kurashi/004/003/001/d00005115.html" class="city-link">世田谷区</a>
    <a href="https://www.google.com/search?q=東京都+各市区町村+犬+登録" class="city-link" style="color:orange;">その他の市区町村（検索）</a>
  </div>

  <button class="pref-btn" onclick="toggleCity('kanagawa')">神奈川県</button>
  <div id="kanagawa" class="city-list">
    <a href="https://www.city.yokohama.lg.jp/kurashi/sumai-kurashi/pet-dobutsu/dog/toroku.html" class="city-link">横浜市</a>
    <a href="https://www.city.kawasaki.jp/350/page/0000017409.html" class="city-link">川崎市</a>
    <a href="https://www.google.com/search?q=神奈川県+各市区町村+犬+登録" class="city-link" style="color:orange;">その他の市区町村（検索）</a>
  </div>

  <button class="pref-btn" onclick="toggleCity('osaka')">大阪府</button>
  <div id="osaka" class="city-list">
    <a href="https://www.city.osaka.lg.jp/kenko/page/0000007323.html" class="city-link">大阪市</a>
    <a href="https://www.city.sakai.lg.jp/kurashi/dobutsu/pet/dog/toroku.html" class="city-link">堺市</a>
    <a href="https://www.google.com/search?q=大阪府+各市区町村+犬+登録" class="city-link" style="color:orange;">その他の市区町村（検索）</a>
  </div>

  <div style="margin-top: 30px; background: white; padding: 20px; border-radius: 15px; border: 1px solid orange;">
    <p style="font-size: 14px; font-weight: bold; margin-top: 0;">🔍 上記以外の地域</p>
    <p style="font-size: 12px; line-height: 1.5;">全国約1,700の自治体の正確な窓口は、厚生労働省の公式リストから各県ごとに確認できます。</p>
    <a href="https://www.mhlw.go.jp/stf/seisakunitsuite/bunya/0000139450.html" style="display:block; background:orange; color:white; text-align:center; padding:12px; border-radius:8px; text-decoration:none; font-weight:bold; margin-top:10px;">厚生労働省 全自治体リスト</a>
  </div>

  <div style="text-align: center; margin-top: 40px;">
    <a href="javascript:history.back()" style="color: #888; font-size: 14px; text-decoration: none;">← 記事に戻る</a>
  </div>
</div>

<script>
function toggleCity(id) {
  const list = document.getElementById(id);
  const allLists = document.querySelectorAll('.city-list');
  allLists.forEach(l => {
    if(l.id !== id) l.style.display = 'none';
  });
  list.style.display = (list.style.display === 'block') ? 'none' : 'block';
}
</script>
