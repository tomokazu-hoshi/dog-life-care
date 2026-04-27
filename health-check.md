---
layout: default
title: 年齢・健康シュミレーター
permalink: /health-check/
---

<style>
  /* 1. 不要なタイトルを完全に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  /* 2. 基本設定 */
  * { box-sizing: border-box; }
  body { 
    font-family: -apple-system, BlinkMacSystemFont, sans-serif; 
    background-color: #f6f8fa; 
    margin: 0; padding: 0; color: #333; overflow-x: hidden;
  }
  
  /* 3. オレンジのヘッダー */
  .custom-header { 
    background: white; padding: 18px 0; text-align: center; border-bottom: 3px solid orange; 
    display: flex; align-items: center; justify-content: center; width: 100%;
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  /* 4. レスポンシブ・コンテナ */
  .container { 
    width: 92%; 
    max-width: 400px; 
    margin: 0 auto; 
    padding: 20px 0 60px; 
  }
  
  /* 5. カードデザイン */
  .card { 
    background: white; border-radius: 15px; box-shadow: 0 4px 12px rgba(0,0,0,0.08); 
    padding: 20px; margin-bottom: 20px; border: 1px solid #eee; width: 100%;
  }
  
  .card-h2 { 
    font-size: 17px; font-weight: bold; margin: 0 0 15px 0; 
    color: #444; border-left: 4px solid orange; padding-left: 10px;
  }

  /* 6. フォーム要素 */
  .form-group { margin-bottom: 15px; }
  label { display: block; font-size: 12px; font-weight: bold; margin-bottom: 6px; color: #666; }
  
  select, input { 
    width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 10px; 
    font-size: 16px; background: #fafafa; -webkit-appearance: none;
  }

  /* 7. オレンジボタン */
  .calc-btn { 
    width: 100%; background: orange; color: white; border: none; padding: 15px; 
    border-radius: 12px; font-size: 16px; font-weight: bold; cursor: pointer; 
    box-shadow: 0 4px 0 #e69500;
  }
  .calc-btn:active { transform: translateY(2px); box-shadow: 0 2px 0 #e69500; }

  /* 8. 結果表示 */
  .result-area { 
    margin-top: 15px; padding: 15px; background: #fff9f0; border-radius: 10px; 
    text-align: center; display: none;
  }
  .result-text { font-size: 17px; font-weight: bold; color: #d9480f; }
  .result-desc { font-size: 12px; color: #777; margin-top: 8px; line-height: 1.4; text-align: left; }

  .kcal-box { display: flex; justify-content: space-around; margin-top: 10px; gap: 10px; }
  .kcal-item { flex: 1; text-align: center; }
  .kcal-val { display: block; font-size: 20px; font-weight: bold; color: orange; }
  .kcal-label { font-size: 10px; color: #888; }
</style>

<div class="custom-header">
  <span class="custom-logo">⌛</span>
  <div class="custom-title">年齢・健康シュミレーター</div>
</div>

<div class="container">

  <section class="card">
    <h2 class="card-h2">🗓️ 年齢診断</h2>
    <div class="form-group">
      <label>犬種サイズ</label>
      <select id="dogSize">
        <option value="small">小型・中型犬（20kg未満）</option>
        <option value="large">大型犬（20kg以上）</option>
      </select>
    </div>
    <div class="form-group">
      <label>現在の年齢（歳）</label>
      <input type="number" id="dogAge" placeholder="例: 5" inputmode="numeric">
    </div>
    <button onclick="calcAge()" class="calc-btn">人間なら何歳？</button>
    <div class="result-area" id="ageResultBox">
      <div id="ageResult" class="result-text"></div>
    </div>
  </section>

  <section class="card">
    <h2 class="card-h2">💧 1日の必要水分量</h2>
    <p style="font-size: 11px; color: #888; margin-bottom: 15px;">体重から1日に必要な「最低限の水分量」を出します</p>
    <div class="form-group">
      <label>現在の体重（kg）</label>
      <input type="number" id="waterWeight" placeholder="例: 10.0" step="0.1" inputmode="decimal">
    </div>
    <button onclick="calcWater()" class="calc-btn">必要量を計算する</button>
    <div class="result-area" id="waterResultBox">
      <div id="waterResult" class="result-text"></div>
      <div class="result-desc">
        ※この数値は「飲み水」と「食事に含まれる水分」の合計です。<br>
        ※急激に飲む量が増えた場合は、病気のサインの可能性があるため獣医師に相談しましょう。
      </div>
    </div>
  </section>

  <section class="card">
    <h2 class="card-h2">🍖 カロリー計算</h2>
    <div class="form-group">
      <label>体重（kg）</label>
      <input type="number" id="weight" placeholder="例: 8.5" step="0.1" inputmode="decimal">
    </div>
    <div class="form-group">
      <label>ライフステージ</label>
      <select id="status">
        <option value="1.6">去勢・避妊済みの成犬</option>
        <option value="1.8">未去勢・未避妊の成犬</option>
        <option value="1.2">高齢・ダイエットが必要</option>
        <option value="3.0">子犬（急成長期）</option>
      </select>
    </div>
    <button onclick="calcAll()" class="calc-btn">カロリーを計算する</button>
    <div class="result-area" id="calResultBox">
      <div class="kcal-box">
        <div class="kcal-item">
          <span class="kcal-label">1日の必要量</span>
          <span id="calResult" class="kcal-val">---</span>
          <span class="kcal-label">kcal</span>
        </div>
        <div class="kcal-item" style="border-left: 1px solid #ddd;">
          <span class="kcal-label">おやつ上限</span>
          <span id="snackResult" class="kcal-val" style="color: #2f9e44;">---</span>
          <span class="kcal-label">kcal</span>
        </div>
      </div>
    </div>
  </section>

  <div style="text-align: center;">
    <a href="{{ '/' | relative_url }}" style="color: #888; font-size: 13px; text-decoration: none;">← ホームに戻る</a>
  </div>
</div>

<script>
function calcAge() {
  const size = document.getElementById('dogSize').value;
  const age = parseFloat(document.getElementById('dogAge').value);
  if(!age) return;
  let humanAge = (size === 'small') ? (age === 1 ? 15 : 24 + (age - 2) * 4) : (age === 1 ? 12 : 22 + (age - 2) * 7);
  document.getElementById('ageResultBox').style.display = 'block';
  document.getElementById('ageResult').innerText = "人間なら約 " + humanAge + " 歳です";
}

function calcWater() {
  const w = parseFloat(document.getElementById('waterWeight').value);
  if(!w) return;
  // 一般的な計算式：体重の0.75乗 × 132、または単純に体重×50〜70ml
  // ここではより安全な 体重(kg) × 50ml〜 を目安に算出
  const minWater = Math.round(w * 50);
  const maxWater = Math.round(w * 70);
  document.getElementById('waterResultBox').style.display = 'block';
  document.getElementById('waterResult').innerText = "目安: " + minWater + " 〜 " + maxWater + " ml";
}

function calcAll() {
  const w = parseFloat(document.getElementById('weight').value);
  const factor = parseFloat(document.getElementById('status').value);
  if(!w) return;
  const rer = 70 * Math.pow(w, 0.75);
  const der = Math.round(rer * factor);
  const snackLimit = Math.round(der * 0.1);
  document.getElementById('calResultBox').style.display = 'block';
  document.getElementById('calResult').innerText = der;
  document.getElementById('snackResult').innerText = snackLimit;
}
</script>
