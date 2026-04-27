---
layout: default
title: 年齢シュミレーター & 健康チェック
permalink: /health-check/
---

<style>
  /* 1. 不要なタイトル（犬種図鑑など）を完全に消す */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  /* 2. 全体の設定 */
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* 3. オレンジのヘッダー */
  .custom-header { background: white; padding: 20px 0; text-align: center; border-bottom: 3px solid orange; display: flex; align-items: center; justify-content: center; }
  .custom-logo { font-size: 24px; margin-right: 10px; }
  .custom-title { font-size: 22px; font-weight: bold; color: orange; margin: 0; }

  /* 4. コンテナとカードのデザイン */
  .container { padding: 20px 15px 60px; max-width: 500px; margin: 0 auto; }
  
  .card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 12px rgba(0,0,0,0.08); 
    padding: 20px; 
    margin-bottom: 25px; 
    border: 1px solid #eee;
  }
  
  .card-h2 { 
    font-size: 18px; 
    font-weight: bold; 
    margin-top: 0; 
    margin-bottom: 15px; 
    color: #444; 
    border-left: 4px solid orange; 
    padding-left: 10px;
    display: flex;
    align-items: center;
  }

  /* 5. 入力フォーム */
  .form-group { margin-bottom: 15px; }
  label { display: block; font-size: 13px; font-weight: bold; margin-bottom: 5px; color: #666; }
  
  select, input { 
    width: 100%; 
    padding: 12px; 
    border: 1px solid #ddd; 
    border-radius: 8px; 
    font-size: 16px; 
    box-sizing: border-box; /* iPhoneでの横幅崩れ防止 */
    background: #fafafa;
  }

  /* 6. オレンジのボタン */
  .calc-btn { 
    width: 100%; 
    background: orange; 
    color: white; 
    border: none; 
    padding: 15px; 
    border-radius: 10px; 
    font-size: 16px; 
    font-weight: bold; 
    cursor: pointer; 
    margin-top: 5px;
    box-shadow: 0 4px 0 #e69500;
  }
  .calc-btn:active { transform: translateY(2px); box-shadow: 0 2px 0 #e69500; }

  /* 7. 結果表示エリア */
  .result-area { 
    margin-top: 15px; 
    padding: 15px; 
    background: #fff9f0; 
    border-radius: 10px; 
    text-align: center; 
    min-height: 20px;
  }
  .result-text { font-size: 18px; font-weight: bold; color: #d9480f; }
  
  .sub-result { font-size: 13px; color: #666; margin-top: 10px; line-height: 1.5; text-align: left; }

  .kcal-box { display: flex; justify-content: space-around; margin-top: 10px; }
  .kcal-item { text-align: center; }
  .kcal-val { display: block; font-size: 22px; font-weight: bold; color: orange; }
  .kcal-label { font-size: 11px; color: #888; }
</style>

<div class="custom-header">
  <span class="custom-logo">⌛</span>
  <div class="custom-title">年齢・健康シュミレーター</div>
</div>

<div class="container">

  <section class="card">
    <h2 class="card-h2">🗓️ 年齢診断（人間換算）</h2>
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
    <button onclick="calcAge()" class="calc-btn">診断結果を見る</button>
    <div class="result-area" id="ageResultBox" style="display:none;">
      <div id="ageResult" class="result-text"></div>
    </div>
  </section>

  <section class="card">
    <h2 class="card-h2">⚖️ 肥満度チェック（BCS）</h2>
    <div class="form-group">
      <label>体型の目安を選択</label>
      <select id="bcsSelect">
        <option value="1">1. 痩せすぎ（肋骨が浮き出ている）</option>
        <option value="2">2. やや痩せ型（くびれが顕著）</option>
        <option value="3" selected>3. 理想的（標準的な体型）</option>
        <option value="4">4. 太り気味（くびれが少ない）</option>
        <option value="5">5. 肥満（肋骨が全く触れない）</option>
      </select>
    </div>
    <button onclick="checkObesity()" class="calc-btn">判定する</button>
    <div class="result-area" id="bcsResultBox" style="display:none;">
      <div id="bcsResult" class="result-text" style="font-size:16px;"></div>
    </div>
  </section>

  <section class="card">
    <h2 class="card-h2">🍖 カロリー & おやつ上限</h2>
    <div class="form-group">
      <label>体重（kg）</label>
      <input type="number" id="weight" placeholder="例: 8.5" step="0.1" inputmode="decimal">
    </div>
    <div class="form-group">
      <label>ライフステージ</label>
      <select id="status">
        <option value="1.6">去勢・避妊済みの成犬</option>
        <option value="1.8">未去勢・未避妊の成犬</option>
        <option value="1.2">肥満傾向・高齢犬</option>
        <option value="1.4">ダイエット中の成犬</option>
        <option value="3.0">子犬（急成長期）</option>
      </select>
    </div>
    <button onclick="calcAll()" class="calc-btn">一括計算する</button>
    
    <div class="result-area" id="calResultBox" style="display:none;">
      <div class="kcal-box">
        <div class="kcal-item">
          <span class="kcal-label">1日の必要カロリー</span>
          <span id="calResult" class="kcal-val">---</span>
          <span class="kcal-label">kcal</span>
        </div>
        <div class="kcal-item" style="border-left: 1px solid #ddd; padding-left: 15px;">
          <span class="kcal-label">おやつの上限(10%)</span>
          <span id="snackResult" class="kcal-val" style="color: #2f9e44;">---</span>
          <span class="kcal-label">kcal</span>
        </div>
      </div>
      <div class="sub-result">
        ※おやつをあげた分、主食（フード）の量を減らして調整してください。
      </div>
    </div>
  </section>

  <div style="text-align: center;">
    <a href="{{ '/' | relative_url }}" style="color: #888; font-size: 14px; text-decoration: none;">← ホームに戻る</a>
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

function checkObesity() {
  const bcs = document.getElementById('bcsSelect').value;
  const msgs = ["", "【痩せすぎ】至急、食事改善や病院での相談を検討してください。", "【やや痩せ型】もう少し脂肪がついても大丈夫です。", "【理想的】素晴らしい！この体型を維持しましょう。", "【太り気味】おやつを控え、適度な運動を心がけましょう。", "【肥満】関節への負担が大きいです。減量を検討してください。"];
  document.getElementById('bcsResultBox').style.display = 'block';
  document.getElementById('bcsResult').innerText = msgs[bcs];
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
