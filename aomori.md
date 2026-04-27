---
layout: default
title: 青森県の自治体一覧
permalink: /registration-search/aomori/
---

<style>
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child, .post-header { display: none !important; }
  html { scroll-behavior: smooth; }
  body { font-family: -apple-system, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; }
  .custom-header { background: white; padding: 18px 0; text-align: center; border-bottom: 3px solid orange; position: sticky; top: 0; z-index: 100; }
  .custom-title { font-size: 18px; font-weight: bold; color: orange; margin: 0; }
  .container { width: 96%; max-width: 500px; margin: 0 auto; padding: 20px 0 60px; }
  .menu-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; margin-bottom: 30px; background: white; padding: 15px; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); }
  .menu-btn { background: #fff9f0; border: 1px solid #ffd8a8; border-radius: 8px; padding: 12px 0; text-align: center; text-decoration: none; color: orange; font-size: 14px; font-weight: bold; }
  .row-section { margin-top: 40px; scroll-margin-top: 80px; }
  .row-title { font-size: 18px; font-weight: bold; color: #444; border-left: 5px solid orange; padding-left: 12px; margin-bottom: 15px; }
  .city-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 6px; }
  .city-btn { background: white; border: 1px solid #ddd; border-radius: 8px; padding: 12px 2px; text-align: center; text-decoration: none; color: #333; font-size: 11px; font-weight: bold; box-shadow: 0 2px 5px rgba(0,0,0,0.05); min-height: 55px; display: flex; align-items: center; justify-content: center; }
</style>

<div class="custom-header"><div class="custom-title">青森県の自治体検索</div></div>
<div class="container">
  <div class="menu-grid">
    <a href="#row-a" class="menu-btn">あ行</a> <a href="#row-ka" class="menu-btn">か行</a> <a href="#row-sa" class="menu-btn">さ行</a>
    <a href="#row-ta" class="menu-btn">た行</a> <a href="#row-na" class="menu-btn">な行</a> <a href="#row-ha" class="menu-btn">は行</a>
    <a href="#row-ma" class="menu-btn">ま行</a> <a href="#row-ya" class="menu-btn">や行</a> <a href="#row-ra" class="menu-btn">ら行</a>
    <a href="#row-wa" class="menu-btn" style="grid-column: span 3;">わ行</a>
  </div>
  <div id="lists"></div>
  <div style="text-align: center; margin-top: 60px;"><a href="{{ '/registration-search/' | relative_url }}" style="color: orange; font-size: 14px; text-decoration: none; font-weight: bold;">← 都道府県を選び直す</a></div>
</div>

<script>
const pref = "青森県";
const data = {
  "あ行": ["青森市", "鰺ヶ沢町", "板柳町", "いなかっ館村", "今別町", "おいらせ町", "大間町", "大鰐町"],
  "か行": ["風間浦村", "黒石市", "五所川原市", "五戸町"],
  "さ行": ["佐井村", "三戸町", "七戸町", "新郷村", "外ヶ浜町"],
  "た行": ["田子町", "田舎館村", "つがる市", "鶴田町", "東北町", "十和田市"],
  "な行": ["中泊町", "南部町", "西目屋村", "野辺地町"],
  "は行": ["八戸市", "東通村", "平内町", "平川市", "深浦町", "藤崎町"],
  "ま行": ["三沢市", "三戸町", "睦沢町", "むつ市"],
  "や行": ["横浜町", "蓬田村"],
  "ら行": ["六戸町", "六ヶ所村"],
};
const ids = {"あ行":"row-a","か行":"row-ka","さ行":"row-sa","た行":"row-ta","な行":"row-na","は行":"row-ha","ま行":"row-ma","や行":"row-ya","ら行":"row-ra"};
const container = document.getElementById('lists');
for (const [row, cities] of Object.entries(data)) {
  const section = document.createElement('section');
  section.id = ids[row]; section.className = 'row-section';
  section.innerHTML = `<div class="row-title">${row}</div><div class="city-grid"></div>`;
  const grid = section.querySelector('.city-grid');
  cities.forEach(city => {
    const a = document.createElement('a'); a.className = 'city-btn';
    a.href = `https://www.google.com/search?q=` + encodeURIComponent(pref + " " + city + " 犬の登録 狂犬病");
    a.innerText = city; grid.appendChild(a);
  });
  container.appendChild(section);
}
</script>
