---
layout: default
title: 初めて犬を迎えられる方へ
permalink: /beginners-guide/
---

<style>
  .guide-body { font-family: -apple-system, sans-serif; color: #333; line-height: 1.8; background: #fff; padding-bottom: 80px; }
  header.site-header, .site-header, .page-title, h1:first-of-type { display: none !important; }

  .guide-menu { background: #fff9f0; border: 2px solid orange; border-radius: 15px; margin: 20px 15px; padding: 15px; }
  .guide-menu-title { font-weight: bold; color: orange; text-align: center; margin-bottom: 10px; }
  .guide-menu ul { list-style: none; padding: 0; margin: 0; }
  .guide-menu a { text-decoration: none; color: #555; font-size: 14px; display: block; padding: 8px 0; border-bottom: 1px dashed #ffd8a8; }
  .guide-menu a::before { content: "🐾"; margin-right: 8px; }

  .guide-section { padding: 30px 15px 10px; scroll-margin-top: 20px; }
  .guide-h2 { background: linear-gradient(to right, orange, #ffcc00); color: white; padding: 12px 15px; border-radius: 8px; font-size: 18px; margin-bottom: 20px; }
  .guide-h3 { border-left: 5px solid orange; padding-left: 10px; margin: 25px 0 10px; font-size: 17px; font-weight: bold; }
  
  .info-card { background: #fefefe; border: 1px solid #eee; border-radius: 12px; padding: 15px; margin: 15px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
  .warning-card { background: #fff5f5; border: 1px solid #ffc9c9; border-radius: 12px; padding: 15px; margin: 15px 0; }
  .price-tag { display: inline-block; background: #fff; border: 1px solid #e03131; color: #e03131; padding: 2px 10px; border-radius: 5px; font-weight: bold; font-size: 13px; margin-bottom: 10px; }

  .btn-orange { display: block; background: orange; color: white !important; text-align: center; padding: 15px; border-radius: 10px; text-decoration: none; font-weight: bold; margin: 20px 0; }
</style>

<div class="guide-body">
  <div style="text-align:center; padding: 30px 0 10px;">
    <h1 style="font-size: 24px; color: orange;">🔰 初めての飼い主さんガイド</h1>
  </div>

  <nav class="guide-menu">
    <div class="guide-menu-title">目次</div>
    <ul>
      <li><a href="#registration">自治体への登録</a></li>
      <li><a href="#microchip">マイクロチップの装着・登録</a></li>
      <li><a href="#vaccine">健康診断と混合ワクチン</a></li>
      <li><a href="#rabies">狂犬病予防接種（年1回）</a></li>
      <li><a href="#filaria">フィラリア予防【最重要】</a></li>
    </ul>
  </nav>

  <section id="registration" class="guide-section">
    <h2 class="guide-h2">自治体への登録</h2>
    <p>ワンちゃんを迎えたら30日以内に、お住まいの市区町村へ登録しましょう。これは法律で決まっている飼い主の義務です。</p>
    <a href="{{ '/registration-search/' | relative_url }}" class="btn-orange">全国の自治体検索はこちら</a>
  </section>

  <section id="filaria" class="guide-section">
    <h2 class="guide-h2" style="background: #e03131;">フィラリア予防【絶対に忘れないで】</h2>
    <div class="warning-card">
      <p style="color: #e03131; font-weight: bold; font-size: 18px; text-align: center;">「薬で100%防げる病気」です</p>
      <p>フィラリアは蚊が媒介する寄生虫です。<strong>「外飼いなら2年で約70%が感染する」</strong>というデータもあるほど、予防なしでは極めてリスクが高い病気です。</p>
      
      <h3 style="color: #c92a2a; font-size: 15px;">なぜ治療が困難なのか？</h3>
      <p style="font-size: 14px;">一度感染すると、フィラリア（細長い虫）は心臓や肺の血管に居座ります。これを薬で一度に殺すと、死骸が血管に詰まって心臓が止まってしまう（肺塞栓症）リスクがあるため、一気に治療することができません。手術で一匹ずつ取り出すのも、ワンちゃんの体に多大な負担と命の危険が伴います。</p>
      <p><strong>「なってから治す」のではなく「月に一度の薬」で100%守ってあげてください。</strong></p>
    </div>
  </section>

  <section id="rabies" class="guide-section">
    <h2 class="guide-h2">狂犬病予防接種（年1回）</h2>
    <p>狂犬病ワクチンは、<strong>1年に1回の接種</strong>が法律で義務付けられています。</p>
    <div class="info-card">
      <p>毎年4月〜6月に自治体から届くハガキを持って病院へ行きましょう。</p>
      <p style="font-size: 13px; color: #666;">※他県の病院で受けた場合は、病院でもらう証明書を持って自治体の窓口へ行き、注射済票（タグ）をもらう必要があります。</p>
    </div>
  </section>

  <section id="microchip" class="guide-section">
    <h2 class="guide-h2">マイクロチップの装着・登録</h2>
    <p>迷子対策の必須アイテムです。</p>
    <div class="info-card">
      <div class="price-tag">費用の目安：3,000円〜10,000円</div>
      <p><strong>保護犬を迎えた場合：</strong><br>前の団体から引き継いだ後、必ず動物病院で装着の有無を確認し、未装着なら装着、装着済みなら「飼い主情報の変更登録」を行ってください。</p>
    </div>
  </section>

  <section id="vaccine" class="guide-section">
    <h2 class="guide-h2">健康診断と混合ワクチン</h2>
    <div class="info-card">
      <p><strong>混合ワクチンとは：</strong><br>ドッグパルボウイルスやジステンパーなど、致死率の高い恐ろしい感染症から守るためのワクチンです。</p>
      <ul>
        <li>ドッグランやペットホテル利用時の必須条件です。</li>
        <li>接種後は数日安静にする必要があるため、予定のない日に打ちましょう。</li>
      </ul>
      <div class="price-tag">費用の目安：5,000円〜10,000円</div>
    </div>
  </section>

  <div style="text-align: center; margin-top: 50px;">
    <a href="{{ '/' | relative_url }}" style="color: orange; font-weight: bold; text-decoration: none;">← ホームに戻る</a>
  </div>
</div>
