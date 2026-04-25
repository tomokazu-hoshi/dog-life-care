---
layout: default
title: 健康チェックツール
---
{% include breadcrumb.html %}

<header class="tc pv3">
  <h1 class="f3 fw9 black">健康チェックツール</h1>
  <p class="f7 gray">愛犬の健康管理にお役立てください</p>
</header>

<div class="ph2 mw7 center">
  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">🗓️ 年齢診断（人間なら何歳？）</h2>
    <div class="mb3">
      <label class="f7 db mb1">犬種サイズ</label>
      <select id="dogSize" class="w-100 pa2 ba b--black-20 br2">
        <option value="small">小型・中型犬（20kg未満）</option>
        <option value="large">大型犬（20kg以上）</option>
      </select>
    </div>
    <div class="mb3">
      <label class="f7 db mb1">現在の年齢</label>
      <input type="number" id="dogAge" class="w-100 pa2 ba b--black-20 br2" placeholder="例: 5">
    </div>
    <button onclick="calcAge()" class="w-100 bg-black white fw6 pv2 br2 dim pointer ba b--black">診断する</button>
    <div id="ageResult" class="mt3 tc f4 fw9 gold"></div>
  </section>

  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">⚖️ 肥満度チェック (BCS)</h2>
    <p class="f7 gray mb3">体に触れた時の感覚を選んでください</p>
    <select id="bcsSelect" class="w-100 pa2 ba b--black-20 br2 mb3">
      <option value="1">肋骨が見えていて、脂肪が全くない</option>
      <option value="2">肋骨を簡単に触れる、上から見て腰にくびれがある</option>
      <option value="3">肋骨を触れる（標準）、適度な腰のくびれ</option>
      <option value="4">脂肪に覆われ肋骨が触れにくい、くびれがほぼない</option>
      <option value="5">厚い脂肪で肋骨が触れない、お腹が垂れている</option>
    </select>
    <button onclick="checkObesity()" class="w-100 bg-black white fw6 pv2 br2 dim pointer ba b--black">チェックする</button>
    <div id="bcsResult" class="mt3 tc f6 fw6"></div>
  </section>

  <section class="bg-white br3 pa3 shadow-4 mb4">
    <h2 class="f5 fw6 mb3 bb b--black-10 pb2">🍖 1日の必要カロリー計算</h2>
    <div class="mb3">
      <label class="f7 db mb1">体重 (kg)</label>
      <input type="number" id="weight" class="w-100 pa2 ba b--black-20 br2" placeholder="例: 10.5" step="0.1">
    </div>
    <div class="mb3">
      <label class="f7 db mb1">ライフステージ</label>
      <select id="status" class="w-100 pa2 ba b--black-20 br2">
        <option value="1.6">去勢・避妊済みの成犬</option>
        <option value="1.8">未去勢・未避妊の成犬</option>
        <option value="1.2">肥満傾向・高齢犬</option>
        <option value="3.0">子犬（成長期）</option>
      </select>
    </div>
    <button onclick="calcCalorie()" class="w-100 bg-black white fw6 pv2 br2 dim pointer ba b--black">計算する</button>
    <div id="calResult" class="mt3 tc f4 fw9 gold"></div>
  </section>
</div>

<script>
// 年齢診断ロジック
function calcAge() {
  const size = document.getElementById('dogSize').value;
  const age = parseFloat(document.getElementById('dogAge').value);
  let humanAge = 0;
  if(!age) return;

  if (size === 'small') {
    if (age === 1) humanAge = 15;
    else humanAge = 24 + (age - 2) * 4;
  } else {
    if (age === 1) humanAge = 12;
    else humanAge = 22 + (age - 2) * 7;
  }
  document.getElementById('ageResult').innerText = "人間なら約 " + humanAge + " 歳です";
}

// 肥満度ロジック
function checkObesity() {
  const bcs = document.getElementById('bcsSelect').value;
  const msgs = [
    "",
    "【痩せすぎ】食事量を増やし、獣医師に相談しましょう。",
    "【やや痩せ型】理想まであと少しです。",
    "【理想的】現在の状態を維持しましょう！",
    "【太り気味】おやつを控え、運動量を増やしましょう。",
    "【肥満】病気のリスクが高まります。ダイエットが必要です。"
  ];
  document.getElementById('bcsResult').innerText = msgs[bcs];
}

// カロリーロジック (RER = 70 * weight^0.75)
function calcCalorie() {
  const w = parseFloat(document.getElementById('weight').value);
  const factor = parseFloat(document.getElementById('status').value);
  if(!w) return;
  
  const rer = 70 * Math.pow(w, 0.75);
  const der = Math.round(rer * factor);
  document.getElementById('calResult').innerText = "1日の目安: " + der + " kcal";
}
</script>

<div class="tc pv4">
  <a href="{{ '/' | relative_url }}" class="f7 gray">← ホームに戻る</a>
</div>
