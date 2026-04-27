---
layout: default
title: 年齢シュミレーター & 健康チェック
permalink: /health-check/
---

<style>
  /* 1. 不要なタイトルを完全に非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  /* 2. 全機種対応のための基本設定 */
  * { box-sizing: border-box; } /* パディングが横幅を突き破らないようにする魔法 */

  body { 
    font-family: -apple-system, BlinkMacSystemFont, sans-serif; 
    background-color: #f6f8fa; 
    margin: 0; 
    padding: 0; 
    color: #333; 
    overflow-x: hidden; /* 横揺れ防止 */
  }
  
  /* 3. オレンジのヘッダー */
  .custom-header { 
    background: white; 
    padding: 18px 0; 
    text-align: center; 
    border-bottom: 3px solid orange; 
    display: flex; 
    align-items: center; 
    justify-content: center; 
    width: 100%;
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  /* 4. 【重要】画面幅に合わせるメインコンテナ */
  .container { 
    width: 92%; /* 画面の92%を使う（左右に4%ずつの余裕） */
    max-width: 400px; /* 大きすぎる画面（iPadなど）でも広がりすぎない */
    margin: 0 auto; /* 常に真ん中に配置 */
    padding: 20px 0 60px; 
  }
  
  /* 5. カードのデザイン */
  .card { 
    background: white; 
    border-radius: 15px; 
    box-shadow: 0 4px 12px rgba(0,0,0,0.08); 
    padding: 18px; 
    margin-bottom: 20px; 
    border: 1px solid #eee;
    width: 100%; /* 親のcontainerに合わせる */
  }
  
  .card-h2 { 
    font-size: 17px; 
    font-weight: bold; 
    margin-top: 0; 
    margin-bottom: 15px; 
    color: #444; 
    border-left: 4px solid orange; 
    padding-left: 10px;
  }

  /* 6. 入力フォーム（スマホで押しやすい高さ） */
  .form-group { margin-bottom: 15px; }
  label { display: block; font-size: 12px; font-weight: bold; margin-bottom: 6px; color: #666; }
  
  select, input { 
    width: 100%; 
    padding: 12px; 
    border: 1px solid #ddd; 
    border-radius: 10px; 
    font-size: 16px; 
    background: #fafafa;
    -webkit-appearance: none; /* iPhone独自のスタイルをリセット */
  }

  /* 7. ボタン */
  .calc-btn { 
    width: 100%; 
    background: orange; 
    color: white; 
    border: none; 
    padding: 15px; 
    border-radius: 12px; 
    font-size: 16px; 
    font-weight: bold; 
    cursor: pointer; 
    box-shadow: 0 4px 0 #e69500;
  }
  .calc-btn:active { transform: translateY(2px); box-shadow: 0 2px 0 #e69500; }

  /* 8. 結果表示 */
  .result-area { 
    margin-top: 15px; 
    padding: 15px; 
    background: #fff9f0; 
    border-radius: 10px; 
    text-align: center; 
    display: none; /* 最初は隠す */
  }
  .result-text { font-size: 17px; font-weight: bold; color: #d9480f; }
  
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
    <h2 class="card-h2">⚖️ 肥満度チェック</h2>
    <div class="form-group">
      <label>体型の目安</label>
      <select id="bcsSelect">
        <option value="1">1. 痩せすぎ</option>
        <option value="2">2. やや痩せ型</option>
        <option value="3" selected>3. 理想的</option>
        <option value="4">4. 太り気味</option>
        <option value="5">5. 肥満</option>
      </select>
    </div>
    <button onclick="checkObesity()" class="calc-btn">体型を判定する</button>
    <div class="result-area" id="bcsResultBox">
      <div id="bcsResult" class="result-text" style="font-size:15px;"></div>
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

function checkObesity() {
  const bcs = document.getElementById('bcsSelect').value;
  const msgs = ["", "【痩せすぎ】食事改善を検討しましょう。", "【やや痩せ型】理想までもう少し！", "【理想的】素晴らしい！維持しましょう。", "【太り気味】おやつを控えて運動を！", "【肥満】関節への負担に注意。減量を。"];
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
