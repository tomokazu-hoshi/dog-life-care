---
layout: default
title: 初めて犬を迎えられる方へ
permalink: /beginners-guide/
---

<style>
  /* 全体設定 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child, .post-header { display: none !important; }
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* 共通ブランドヘッダー（固定を解除） */
  .custom-header { 
    background: white; padding: 20px 0; text-align: center; border-bottom: 3px solid orange; 
    display: flex; align-items: center; justify-content: center;
    /* スクロールで流れるように固定解除 */
    position: relative; 
  }

  .guide-body { line-height: 1.8; background: #fff; padding-bottom: 80px; }

  /* 記事トップのナビメニュー */
  .guide-menu { background: #fff9f0; border: 2px solid orange; border-radius: 15px; margin: 20px 15px; padding: 15px; }
  .guide-menu-title { font-weight: bold; color: orange; text-align: center; margin-bottom: 10px; font-size: 16px; }
  .guide-menu ul { list-style: none; padding: 0; margin: 0; }
  .guide-menu li { margin-bottom: 8px; border-bottom: 1px dashed #ffd8a8; padding-bottom: 5px; }
  .guide-menu a { text-decoration: none; color: #555; font-size: 14px; display: block; }
  .guide-menu a::before { content: "▶"; color: orange; margin-right: 8px; }

  /* コンテンツ設定 */
  .guide-section { padding: 30px 15px 10px; scroll-margin-top: 20px; }
  .guide-h2 { background: orange; color: white; padding: 10px 15px; border-radius: 5px; font-size: 18px; margin-bottom: 20px; }
  .guide-h3 { border-left: 5px solid orange; padding-left: 10px; margin: 25px 0 10px; font-size: 16px; font-weight: bold; }
  
  /* スケジュールリスト */
  .timeline { border-left: 2px solid orange; margin-left: 10px; padding-left: 20px; position: relative; }
  .timeline-item { margin-bottom: 30px; position: relative; }
  .timeline-item::before { content: ""; width: 12px; height: 12px; background: orange; border-radius: 50%; position: absolute; left: -27px; top: 8px; }
  .time-label { font-weight: bold; color: orange; font-size: 14px; }

  /* テーブル（年間スケジュール） */
  .schedule-table { width: 100%; border-collapse: collapse; margin-top: 15px; font-size: 13px; background: white; }
  .schedule-table th, .schedule-table td { border: 1px solid #ddd; padding: 10px 5px; text-align: center; }
  .schedule-table th { background: #fff4e6; color: #d9480f; }
  
  /* リンクボタン */
  .link-btn { display: inline-block; background: orange; color: white !important; padding: 12px 20px; border-radius: 25px; text-decoration: none; font-size: 14px; font-weight: bold; margin-top: 10px; box-shadow: 0 3px 0 #e69500; }
  
  /* 強調ボックス */
  .filaria-warning { background: #fff5f5; border: 2px solid #ffc9c9; border-radius: 10px; padding: 15px; margin-top: 20px; }
  .price-text { font-size: 12px; color: #e03131; font-weight: bold; }
</style>

<div class="custom-header">
  <span class="custom-logo">🐶</span>
  <div class="custom-title">ワンライフ・ナビ</div>
</div>

<div class="guide-body">
  <div style="text-align:center; padding: 30px 0 10px;">
    <h1 style="font-size: 22px; color: orange;">🔰 初めての飼い主さんガイド</h1>
    <p style="font-size: 13px; color: #888;">〜愛犬と幸せに暮らすための全手順〜</p>
  </div>

  <nav class="guide-menu">
    <div class="guide-menu-title">目次（タップで移動）</div>
    <ul>
      <li><a href="#first-steps">迎えてすぐにやること（法律・手続き）</a></li>
      <li><a href="#growth-flow">成長スケジュール（生後〜1年まで）</a></li>
      <li><a href="#annual-schedule">毎年の恒例行事（年間スケジュール）</a></li>
    </ul>
  </nav>

  <section id="first-steps" class="guide-section">
    <h2 class="guide-h2">1. 迎えてすぐにやること</h2>
    <p>法律で定められた手続きと、身分証明となるマイクロチップについて解説します。</p>

    <h3 class="guide-h3">市町村への登録</h3>
    <p>生後90日を過ぎた犬を飼い始めたら、30日以内に自治体への登録が義務付けられています。</p>
    <a href="{{ '/registration-search/' | relative_url }}" class="link-btn">各自治体の検索はこちら</a>

    <h3 class="guide-h3">マイクロチップの装着・登録</h3>
    <p>迷子や災害時の唯一の身分証明です。<br>
    <span class="price-text">おおよその費用：3,000円〜10,000円程度</span></p>
    <p><strong>保護犬を迎えた場合：</strong><br>必ず動物病院で装着の有無を確認してもらいましょう。未装着なら装着、装着済みなら「飼い主情報の変更登録」を必ず行ってください。情報の紐付けがないと、万が一の際に見つかりません。</p>
  </section>

  <section id="growth-flow" class="guide-section">
    <h2 class="guide-h2">2. 成長スケジュール</h2>
    <div class="timeline">
      <div class="timeline-item">
        <div class="time-label">迎えてすぐ</div>
        <p><strong>健康診断と混合ワクチン</strong><br>
        まずは動物病院へ。便検査や触診を受け、健康状態を確認しましょう。</p>
        
        <div style="background: #f9f9f9; padding: 10px; border-radius: 8px; font-size: 14px; margin-top: 10px;">
          <strong>混合ワクチンとは？</strong><br>
          ジステンパーやパルボウイルスなど、命に関わる強力な感染症を防ぐための任意のワクチンです。ドッグランやペットホテル、トリミングサロンを利用する際に「接種証明書」の提示が必須となることが多いため、必ず取得して持参しましょう。<br>
          <span class="price-text">おおよその費用：5,000円〜10,000円程度</span>
        </div>
      </div>
      
      <div class="timeline-item">
        <div class="time-label">生後3〜4ヶ月</div>
        <p><strong>狂犬病予防接種</strong><br>
        法律で義務付けられている<strong>年1回</strong>の注射です。自治体から届くハガキを持参しましょう。<br>
        <strong>※他県の病院で受ける場合：</strong><br>
        他県のかかりつけ医等で接種した場合は、発行された証明書を自分の住む自治体窓口へ出し、「注射済票」を別途受け取る必要があります。</p>
      </div>
      
      <div class="timeline-item">
        <div class="time-label">生後6ヶ月〜</div>
        <p><strong>去勢・避妊手術</strong><br>
        病気予防やストレス軽減のために検討します。<br>
        費用：3万〜6万円程度（助成金が出る地域もあります）</p>
      </div>
    </div>
  </section>

  <section id="annual-schedule" class="guide-section">
    <h2 class="guide-h2">3. 1年間のスケジュール</h2>
    <p>健康維持のために、毎年決まった時期に行う予防です。</p>

    <table class="schedule-table">
      <thead>
        <tr>
          <th>予防項目</th>
          <th>時期・頻度</th>
          <th>目的</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td style="font-weight:bold;">狂犬病注射</td>
          <td>4月〜6月（年1回）</td>
          <td>法律義務</td>
        </tr>
        <tr>
          <td style="font-weight:bold; color:#e03131;">フィラリア薬</td>
          <td>5月〜12月（毎月）</td>
          <td>命を守る最重要予防</td>
        </tr>
        <tr>
          <td style="font-weight:bold;">混合ワクチン</td>
          <td>年1回</td>
          <td>感染症予防</td>
        </tr>
        <tr>
          <td style="font-weight:bold;">ノミ・ダニ予防</td>
          <td>通年（毎月）</td>
          <td>寄生虫の予防</td>
        </tr>
      </tbody>
    </table>

    <div class="filaria-warning">
      <p style="color: #e03131; font-weight: bold; margin: 0 0 10px 0;">🔴 フィラリア予防の重要性</p>
      <p style="font-size: 14px;">フィラリアは、蚊が媒介する恐ろしい寄生虫です。<strong>「外飼いなら2年で約70%が感染する」</strong>とも言われ、予防をしなければ極めて危険です。</p>
      <p style="font-size: 14px;"><strong>なぜ治療が困難なのか？</strong><br>
      感染すると心臓や肺の血管に「そうめん」のような虫が居座ります。薬で一気に殺すと、その死骸が血管を塞いで突然死を招くリスクがあるため、簡単には治療できません。手術で一匹ずつ釣り出すのも、ワンちゃんにとって命がけの負担となります。</p>
      <p style="font-size: 14px; font-weight: bold;">「毎月の薬で100%防げる病気」です。絶対に忘れないでください。</p>
    </div>

    <p style="font-size: 12px; color: #666; margin-top: 15px;">※各種費用は動物病院やワンちゃんの体重によって異なります。</p>
  </section>

  <div style="text-align: center; margin-top: 50px;">
    <a href="{{ '/' | relative_url }}" style="color: orange; font-weight: bold; text-decoration: none;">← ホームに戻る</a>
  </div>
</div>
