---
layout: default
title: 北海道の自治体一覧
permalink: /registration-search/hokkaido/
---

<style>
  /* 1. 不要なタイトルを完全に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child, .post-header { 
    display: none !important; 
  }

  html { scroll-behavior: smooth; }
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* オレンジのヘッダー（固定） */
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
  <div class="custom-title">北海道の自治体検索</div>
</div>

<div class="container">
  <div class="step-label" style="text-align:center; font-size:12px; color:#888; margin-bottom:10px;">STEP 3：市区町村を選択してください</div>
  
  <div class="menu-grid">
    <a href="#row-a" class="menu-btn">あ行</a> <a href="#row-ka" class="menu-btn">か行</a> <a href="#row-sa" class="menu-btn">さ行</a>
    <a href="#row-ta" class="menu-btn">た行</a> <a href="#row-na" class="menu-btn">な行</a> <a href="#row-ha" class="menu-btn">は行</a>
    <a href="#row-ma" class="menu-btn">ま行</a> <a href="#row-ya" class="menu-btn">や行</a> <a href="#row-ra" class="menu-btn">ら行</a>
    <a href="#row-wa" class="menu-btn" style="grid-column: span 3;">わ行</a>
  </div>

  <div id="lists"></div>

  <div style="text-align: center; margin-top: 60px;">
    <a href="{{ '/registration-search/' | relative_url }}" style="color: orange; font-size: 14px; text-decoration: none; font-weight: bold;">← 都道府県を選び直す</a>
  </div>
</div>

<script>
// 北海道 全179市町村データ
const data = {
  "あ行": ["愛別町", "赤井川村", "赤平市", "旭川市", "芦別市", "足寄町", "厚真町", "厚岸町", "厚沢部町", "網走市", "安平町", "池田町", "石狩市", "今金町", "岩見沢市", "岩内町", "浦河町", "浦臼町", "浦幌町", "雨竜町", "江差町", "枝幸町", "恵庭市", "江別市", "えりも町", "遠軽町", "遠別町", "雄武町", "大空町", "奥尻町", "置戸町", "興部町", "長万部町", "小樽市", "音更町", "乙部町", "音威子府村", "帯広市", "小平町"],
  "か行": ["上砂川町", "上川町", "上士幌町", "上ノ国町", "上富良野町", "神恵内村", "木古内町", "北広島市", "北見市", "喜茂別町", "京極町", "共和町", "清里町", "釧路市", "釧路町", "倶知安町", "栗山町", "黒松内町", "剣淵町", "小清水町"],
  "さ行": ["札幌市", "様似町", "更別村", "猿払村", "佐呂間町", "鹿追町", "鹿部町", "色丹村", "標茶町", "士別市", "標津町", "標津町", "清水町", "占冠村", "下川町", "積丹町", "斜里町", "初山別村", "白老町", "白糠町", "知内町", "新篠津村", "新得町", "新十津川町", "寿都町"],
  "た行": ["大樹町", "鷹栖町", "滝川市", "滝上町", "秩父別町", "千歳市", "月形町", "津別町", "鶴居村", "天塩町", "弟子屈町", "当別町", "当麻町", "洞爺湖町", "苫小牧市", "苫前町", "豊浦町", "豊頃町", "豊富町"],
  "な行": ["奈井江町", "中川町", "中札内村", "中標津町", "中頓別町", "長沼町", "名寄市", "七飯町", "南幌町", "仁木町", "西興部村", "ニセコ町", "沼田町", "登別市"],
  "は行": ["函館市", "羽幌町", "浜中町", "浜頓別町", "美瑛町", "美唄市", "美深町", "美幌町", "比布町", "東神楽町", "東川町", "日高町", "広尾町", "比布町", "深川市", "富良野市", "古平町", "別海町", "北竜町", "幌加内町", "幌延町", "本別町"],
  "ま行": ["幕別町", "増毛町", "真狩村", "松前町", "三笠市", "南富良野町", "むかわ町", "室蘭市", "芽室町", "妹背牛町", "森町", "紋別市"],
  "や行": ["八雲町", "夕張市", "由仁町", "余市町", "湧別町", "由仁町"],
  "ら行": ["羅臼町", "蘭越町", "陸別町", "利尻町", "利尻富士町", "留寿都村", "留萌市"],
  "わ行": ["稚内市", "和寒町"]
};

const ids = {"あ行":"row-a","か行":"row-ka","さ行":"row-sa","た行":"row-ta","な行":"row-na","は行":"row-ha","ま行":"row-ma","や行":"row-ya","ら行":"row-ra","わ行":"row-wa"};

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
    
    // 確実に公式HPが出るよう「自治体名＋犬の登録」でGoogleの検索結果へ
    a.href = `https://www.google.com/search?q=` + encodeURIComponent("北海道 " + city + " 犬の登録 狂犬病");
    
    a.innerText = city;
    grid.appendChild(a);
  });
  container.appendChild(section);
}
</script>
