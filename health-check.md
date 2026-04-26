---
layout: default
title: 健康チェックツール
permalink: /health-check/
---

<header class="tc pv3 bg-white br3 shadow-4 mb3">
  <h1 class="f3 fw9 black">健康チェックツール</h1>
  <p class="f7 gray">診断・計算結果を日々のケアに役立てましょう</p>
</header>

<div class="ph2 mw7 center">
  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">🗓️ 年齢診断（人間換算）</h2>
    <div class="mb3">
      <label class="f7 db mb1 fw6">犬種サイズ</label>
      <select id="dogSize" class="w-100 pa2 ba b--black-20 br2">
        <option value="small">小型・中型犬（20kg未満）</option>
        <option value="large">大型犬（20kg以上）</option>
      </select>
    </div>
    <div class="mb3">
      <label class="f7 db mb1 fw6">現在の年齢（歳）</label>
      <input type="number" id="dogAge" class="w-100 pa2 ba b--black-20 br2" placeholder="例: 5" inputmode="numeric">
    </div>
    <button onclick="calcAge()" class="w-100 bg-black white fw6 pv3 br2 dim pointer ba b--black">診断結果を見る</button>
    <div id="ageResult" class="mt3 tc f4 fw9 gold"></div>
  </section>

  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">⚖️ 肥満度チェック（BCS）</h2>
    <p class="f7 gray mb3">肋骨の触り心地などから判定します</p>
    <select id="bcsSelect" class="w-100 pa2 ba b--black-20 br2 mb3">
      <option value="1">1. 痩せすぎ（肋骨が浮き出ている）</option>
      <option value="2">2. やや痩せ型（くびれが顕著）</option>
      <option value="3">3. 理想的（標準的な体型）</option>
      <option value="4">4. 太り気味（くびれが少ない）</option>
      <option value="5">5. 肥満（肋骨が全く触れない）</option>
    </select>
    <button onclick="checkObesity()" class="w-100 bg-black white fw6 pv3 br2 dim pointer ba b--black">判定する</button>
    <div id="bcsResult" class="mt3 tc f6 fw6 lh-copy"></div>
  </section>

  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">🍖 必要カロリー ＆ おやつ上限</h2>
    <p class="f7 gray mb3">体重とライフステージから算出します</p>
    <div class="mb3">
      <label class="f7 db mb1 fw6">体重（kg）</label>
      <input type="number" id="weight" class="w-100 pa2 ba b--black-20 br2" placeholder="例: 8.5" step="0.1" inputmode="decimal">
    </div>
    <div class="mb3">
      <label class="f7 db mb1 fw6">ライフステージ</label>
      <select id="status" class="w-100 pa2 ba b--black-20 br2">
        <option value="1.6">去勢・避妊済みの成犬</option>
        <option value="1.8">未去勢・未避妊の成犬</option>
        <option value="1.2">肥満傾向・高齢犬</option>
        <option value="1.4">ダイエット中の成犬</option>
        <option value="3.0">子犬（急成長期）</option>
      </select>
    </div>
    <button onclick="calcAll()" class="w-100 bg-black white fw6 pv3 br2 dim pointer ba b--black">一括計算する</button>
    
    <div class="mt4 pa3 bg-near-white br2">
      <div class="mb3 tc">
        <p class="f7 mb1 gray">1日の必要エネルギー（DER）</p>
        <div id="calResult" class="f3 fw9 gold">--- kcal</div>
      </div>
      <div class="tc bt b--black-10 pt3">
        <p class="f7 mb1 gray">今日のおやつ上限（10%以内）</p>
        <div id="snackResult" class="f3 fw9 dark-green">--- kcal</div>
        <p class="f8 gray mt2 lh-copy">※おやつをあげた分、主食（フード）の量を減らして調整してください。</p>
      </div>
    </div>
    <p class="f8 gray mt3 tc">計算式: 70 × (体重)^0.75 × 係数</p>
  </section>
</div>

<script>
function calcAge() {
  const size = document.getElementById('dogSize').value;
  const age = parseFloat(document.getElementById('dogAge').value);
  if(!age) return;
  let humanAge = (size === 'small') ? (age === 1 ? 15 : 24 + (age - 2) * 4) : (age === 1 ? 12 : 22 + (age - 2) * 7);
  document.getElementById('ageResult').innerText = "人間なら約 " + humanAge + " 歳です";
}

function checkObesity() {
  const bcs = document.getElementById('bcsSelect').value;
  const msgs = ["", "【痩せすぎ】至急、食事改善や健康診断を検討してください。", "【やや痩せ型】もう少しお肉がついても大丈夫です。", "【理想的】素晴らしい！この体型を維持しましょう。", "【太り気味】おやつを減らし、適度な運動を心がけてください。", "【肥満】関節への負担が大きいです。"];
  document.getElementById('bcsResult').innerText = msgs[bcs];
}

function calcAll() {
  const w = parseFloat(document.getElementById('weight').value);
  const factor = parseFloat(document.getElementById('status').value);
  if(!w) return;
  const rer = 70 * Math.pow(w, 0.75);
  const der = Math.round(rer * factor);
  const snackLimit = Math.round(der * 0.1);
  document.getElementById('calResult').innerText = der + " kcal";
  document.getElementById('snackResult').innerText = snackLimit + " kcal";
}
</script>

<div class="tc pv4">
  <a href="{{ '/' | relative_url }}" class="f7 gray">← ホームに戻る</a>
</div>
