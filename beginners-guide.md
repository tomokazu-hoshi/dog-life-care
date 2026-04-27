---
layout: default
title: 初めて犬を迎えられる方へ
permalink: /beginners-guide/
---

<style>
  /* 全体設定 */
  .guide-body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; color: #333; line-height: 1.8; background: #fff; padding-bottom: 80px; }
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { display: none !important; }

  /* 目次メニュー */
  .guide-menu { background: #fff9f0; border: 2px solid orange; border-radius: 15px; margin: 20px 15px; padding: 18px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); }
  .guide-menu-title { font-weight: bold; color: orange; text-align: center; margin-bottom: 12px; font-size: 17px; }
  .guide-menu ul { list-style: none; padding: 0; margin: 0; }
  .guide-menu li { margin-bottom: 10px; border-bottom: 1px dashed #ffd8a8; padding-bottom: 8px; }
  .guide-menu a { text-decoration: none; color: #444; font-size: 15px; display: block; font-weight: bold; }
  .guide-menu a::before { content: "🐾"; margin-right: 10px; }

  /* コンテンツ */
  .guide-section { padding: 40px 15px 10px; scroll-margin-top: 20px; }
  .guide-h2 { background: linear-gradient(to right, orange, #ffcc00); color: white; padding: 12px 15px; border-radius: 8px; font-size: 18px; margin-bottom: 20px; box-shadow: 0 4px 10px rgba(255,165,0,0.2); }
  .guide-h3 { border-left: 6px solid orange; padding-left: 12px; margin: 30px 0 15px; font-size: 17px; font-weight: bold; color: #222; }
  
  /* 強調カード */
  .info-card { background: #fefefe; border: 1px solid #eee; border-radius: 12px; padding: 15px; margin: 15px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
  .warning-card { background: #fff5f5; border: 2px solid #ffc9c9; border-radius: 12px; padding: 18px; margin: 20px 0; }
  .price-tag { display: inline-block; background: #fff; border: 1px solid #e03131; color: #e03131; padding: 2px 10px; border-radius: 5px; font-weight: bold; font-size: 13px; margin-bottom: 10px; }

  /* 成長スケジュール（タイムライン） */
  .timeline { border-left: 3px solid orange; margin-left: 10px; padding-left: 25px; position: relative; }
  .timeline-item { margin-bottom: 35px; position: relative; }
  .timeline-item::before { content: ""; width: 14px; height: 14px; background: orange; border-radius: 50%; position: absolute; left: -34px; top: 7px; border: 3px solid white; box-shadow: 0 0 0 2px orange; }
  .time-label { font-weight: bold; color: orange; font-size: 16px; display: block; margin-bottom: 5px; }

  /* 表（年間スケジュール） */
  .schedule-table { width: 100%; border-collapse: collapse; margin: 20px 0; font-size: 13px; background: white; }
  .schedule-table th, .schedule-table td { border: 1px solid #ddd; padding: 12px 8px; text-align: center; line-height: 1.4; }
  .schedule-table th { background: #fff4e6; color: #d9480f; font-weight: bold; }
  
  .btn-search { display: block; background: orange; color: white !important; text-align: center; padding: 16px; border-radius: 12px; text-decoration: none; font-weight: bold; margin: 25px 0; box-shadow: 0 4px 0 #e69500; }
  .btn-search:active { transform: translateY(2px); box-shadow: 0 2px 0 #e69500; }
</style>

<div class="guide-body">
  <div style="text-align:center; padding: 40px 0 10px;">
    <h1 style="font-size: 24px; color: orange; margin-bottom: 8px;">🔰 はじめての飼い主さんガイド</h1>
    <p style="font-size: 14px; color: #666;">愛犬と幸せに暮らすために、絶対に知っておくべきこと</p>
  </div>

  <nav class="guide-menu">
    <div class="guide-menu-title">目次（タップで移動）</div>
    <ul>
      <li><a href="#welcome-steps">1. 迎えてからのスケジュール</a></li>
      <li><a href="#annual-steps">2. 毎年のスケジュール（表）</a></li>
      <li><a href="#registration">3. 自治体への登録</a></li>
      <li><a href="#filaria">4. フィラリア予防【最重要】</a></li>
      <li><a href="#vaccine">5. 健康診断と混合ワクチン</a></li>
      <li><a href="#rabies">6. 狂犬病予防接種（年1回）</a></li>
      <li><a href="#microchip">7. マイクロチップの装着・登録</a></li>
    </ul>
  </nav>

  <section id="welcome-steps" class="guide-section">
    <h2 class="guide-h2">1. 迎えてからのスケジュール</h2>
    <div class="timeline">
      <div class="timeline-item">
        <span class="time-label">当日 〜 3日目</span>
        <p><strong>環境に慣らす時期</strong><br>無理に構わず、静かに見守りましょう。まずは新しい家の匂いや音に慣れてもらうことが最優先です。</p>
      </div>
      <div class="timeline-item">
        <span class="time-label">1週間以内</span>
        <p><strong>初めての健康診断（動物病院へ）</strong><br>便検査（寄生虫確認）や触診を受けましょう。ここで混合ワクチンの計画も立てます。</p>
      </div>
      <div class="timeline-item">
        <span class="time-label">30日以内</span>
        <p><strong>自治体への登録</strong><br>法律で決まっている手続きです。お住まいの市町村で登録を行いましょう。</p>
      </div>
      <div class="timeline-item">
        <span class="time-label">半年 〜 1年</span>
        <p><strong>去勢・避妊手術の検討</strong><br>将来の病気予防のために。自治体によっては助成金が出る場合もあります。</p>
      </div>
    </div>
  </section>

  <section id="annual-steps" class="guide-section">
    <h2 class="guide-h2">2. 毎年のスケジュール</h2>
    <p>ワンちゃんの健康を守るために、毎年決まった時期に繰り返す大切な習慣です。</p>
    
    <table class="schedule-table">
      <thead>
        <tr>
          <th>予防項目</th>
          <th>時期</th>
          <th>頻度・目的</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td style="font-weight:bold;">狂犬病予防</td>
          <td>4月〜6月</td>
          <td>年1回<br><span style="font-size:11px; color:#888;">(法律で義務)</span></td>
        </tr>
        <tr>
          <td style="font-weight:bold; color:#e03131;">フィラリア薬</td>
          <td>5月〜12月</td>
          <td>毎月1回<br><span style="font-size:11px; color:#888;">(100%予防可能)</span></td>
        </tr>
        <tr>
          <td style="font-weight:bold;">混合ワクチン</td>
          <td>年1回</td>
          <td>任意の予防<br><span style="font-size:11px; color:#888;">(ドッグラン等に必要)</span></td>
        </tr>
        <tr>
          <td style="font-weight:bold;">ノミ・ダニ予防</td>
          <td>通年</td>
          <td>毎月1回<br><span style="font-size:11px; color:#888;">(寄生虫の予防)</span></td>
        </tr>
      </tbody>
    </table>
  </section>

  <section id="registration" class="guide-section">
    <h2 class="guide-h2">3. 自治体への登録</h2>
    <p>法律により、生後90日を過ぎた犬を飼い始めたら30日以内に市区町村へ登録しなければなりません。</p>
    <a href="{{ '/registration-search/' | relative_url }}" class="btn-search">全国の自治体検索ページへ</a>
  </section>

  <section id="filaria" class="guide-section">
    <h2 class="guide-h2" style="background: #e03131;">4. フィラリア予防【最重要】</h2>
    <div class="warning-card">
      <p style="color: #e03131; font-weight: bold; font-size: 19px; text-align: center; margin-bottom: 15px;">「月に一回の薬で100%守れます」</p>
      <p>フィラリアは、蚊が媒介する寄生虫です。<strong>「外飼いなら2年で約70%が感染する」</strong>という非常に恐ろしい病気です。</p>
      
      <h3 class="guide-h3">なぜ感染すると危険なのか？</h3>
      <p>心臓や肺の血管に「そうめん」のような長い虫が居座ります。一度感染すると、治療は非常に困難です。</p>
      <ul>
        <li><strong>薬で一気に殺せない：</strong>死んだ虫が血管に詰まり、突然死（肺塞栓症）を招くリスクがあります。</li>
        <li><strong>手術の負担：</strong>首の血管から器具を入れて虫を釣り出す手術は、ワンちゃんの体力を激しく消耗させます。</li>
      </ul>
      <p><strong>「なってから治す」のは至難の業。毎月の予防で、確実に防ぎましょう。</strong></p>
    </div>
  </section>

  <section id="vaccine" class="guide-section">
    <h2 class="guide-h2">5. 健康診断と混合ワクチン</h2>
    <div class="info-card">
      <div class="price-tag">費用の目安：5,000円〜10,000円</div>
      <p><strong>混合ワクチンとは：</strong><br>ジステンパーやパルボウイルスなど、命に関わる強力な感染症を防ぐためのものです。</p>
      <ul>
        <li>ドッグラン、ペットホテル、トリミングサロンなどの利用時に、**接種証明書**の提示を求められることがほとんどです。</li>
        <li>動物病院で便検査や触診を一緒に受けて、証明書を取得しておきましょう。</li>
      </ul>
    </div>
  </section>

  <section id="rabies" class="guide-section">
    <h2 class="guide-h2">6. 狂犬病予防接種（年1回）</h2>
    <div class="info-card">
      <p><strong>1年に1回</strong>の接種が法律で義務付けられています。</p>
      <p>自治体から届くハガキを持参しましょう。他県のかかりつけ医などで接種した場合は、もらった証明書を**お住まいの自治体窓口**へ持っていき、「注射済票」を別途発行してもらう必要があります。</p>
    </div>
  </section>

  <section id="microchip" class="guide-section">
    <h2 class="guide-h2">7. マイクロチップの装着・登録</h2>
    <div class="info-card">
      <div class="price-tag">費用の目安：3,000円〜10,000円</div>
      <p>迷子や災害時の唯一の身分証明書です。**保護犬を迎えた場合**は、必ず病院で装着の有無を確認し、未装着なら装着、装着済みなら「飼い主情報の登録変更」を必ず行ってください。</p>
    </div>
  </section>

  <div style="text-align: center; margin-top: 50px;">
    <a href="{{ '/' | relative_url }}" style="color: orange; font-weight: bold; text-decoration: none;">← ホームに戻る</a>
  </div>
</div>
