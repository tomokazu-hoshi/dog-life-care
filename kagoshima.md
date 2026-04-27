---
layout: default
title: 鹿児島県の自治体一覧
permalink: /registration-search/kagoshima/
---

<style>
  /* 不要なタイトルを完全に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child, .post-header { 
    display: none !important; 
  }

  html { scroll-behavior: smooth; }
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* オレンジのヘッダー */
  .custom-header { 
    background: white; padding: 18px 0; text-align: center; border-bottom: 3px solid orange; 
    position: sticky; top: 0; z-index: 100;
  }
  .custom-title { font-size: 18px; font-weight: bold; color: orange; margin: 0; }

  .container { width: 96%; max-width: 500px; margin: 0 auto; padding: 20px 0 60px; }
  
  /* 50音メニュー 3列 */
  .menu-grid { 
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; 
    margin-bottom: 30px; background: white; padding: 15px; border-radius: 15px; 
    box-shadow: 0 4px 10px rgba(0,0,0,0.05); 
  }
  .menu-btn { 
    background: #fff9f0; border: 1px solid #ffd8a8; border-radius: 8px; padding: 12px 0;
    text-align: center; text-decoration: none; color: orange; font-size: 14px; font-weight: bold;
  }

  /* 市町村リスト セクション */
  .row-section { margin-top: 40px; scroll-margin-top: 80px; }
  .row-title { font-size: 18px; font-weight: bold; color: #444; border-left: 5px solid orange; padding-left: 12px; margin-bottom: 15px; }
  
  /* 市町村ボタン 3列 */
  .city-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; }
  .city-btn { 
    background: white; border: 1px solid #ddd; border-radius: 8px; 
    padding: 12px 2px; text-align: center; text-decoration: none; 
    color: #333; font-size: 11px; font-weight: bold;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05); min-height: 55px; 
    display: flex; align-items: center; justify-content: center;
  }
  .city-btn:active { background: #fff9f0; border-color: orange; color: orange; transform: scale(0.95); }
</style>

<div class="custom-header">
  <div class="custom-title">鹿児島県の自治体検索</div>
</div>

<div class="container">
  <div class="step-label" style="text-align:center; font-size:12px; color:#888; margin-bottom:10px;">STEP 3：市区町村を選択してください</div>
  
  <div class="menu-grid">
    <a href="#row-a" class="menu-btn">あ行</a> <a href="#row-ka" class="menu-btn">か行</a> <a href="#row-sa" class="menu-btn">さ行</a>
    <a href="#row-ta" class="menu-btn">た行</a> <a href="#row-na" class="menu-btn">な行</a> <a href="#row-ha" class="menu-btn">は行</a>
    <a href="#row-ma" class="menu-btn">ま行</a> <a href="#row-ya" class="menu-btn">や行</a> <a href="#row-wa" class="menu-btn">わ行</a>
  </div>

  <div id="lists"></div>

  <div style="text-align: center; margin-top: 60px;">
    <a href="{{ '/registration-search/' | relative_url }}" style="color: orange; font-size: 14px; text-decoration: none; font-weight: bold;">← 都道府県を選び直す</a>
  </div>
</div>

<script>
const pref = "鹿児島県";
const data = {
  "あ行": ["姶良市", "阿久根市", "天城町", "奄美市", "伊佐市", "出水市", "いちき串木野市", "指宿市", "伊仙町", "宇検村", "大崎町"],
  "か行": ["鹿児島市", "鹿屋市", "喜界町", "霧島市", "肝付町", "錦江町"],
  "さ行": ["薩摩川内市", "さつま町", "志布志市", "瀬戸内町", "曽於市"],
  "た行": ["垂水市", "龍郷町", "知名町", "徳之島町", "十島村"],
  "な行": ["中種子町", "長島町", "西之表市"],
  "は行": ["東串良町", "日置市"],
  "ま行": ["枕崎市", "三島村", "南九州市", "南さつま市", "南種子町", "南大隅町"],
  "や行": ["屋久島町", "大和村", "与論町", "湧水町"],
  "わ行": ["和泊町"]
};

const ids = {"あ行":"row-a","か行":"row-ka","さ行":"row-sa","た行":"row-ta","な行":"row-na","は行":"row-ha","ま行":"row-ma","や行":"row-ya","わ行":"row-wa"};

const container = document.getElementById('lists');
for (const [row, cities] of Object.entries(data)) {
  const section = document.createElement('section');
  section.id = ids[row];
  section.className = 'row-section';
  section.innerHTML = `<div class="row-title">${row}</div><div class="city-grid"></div>`;
  const grid = section.querySelector('.city-grid');
  
  cities.forEach(city => {
    const a = document.createElement('a');
    a.className = 'city-btn';
    a.href = `https://www.google.com/search?q=` + encodeURIComponent(pref + " " + city + " 犬の登録 狂犬病");
    a.innerText = city;
    grid.appendChild(a);
  });
  container.appendChild(section);
}
</script>
