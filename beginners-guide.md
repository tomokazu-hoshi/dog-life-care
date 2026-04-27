---
layout: default
title: 初めて犬を迎えられる方へ
permalink: /beginners-guide/
---

<style>
  /* 全体設定 */
  .guide-body { font-family: -apple-system, sans-serif; color: #333; line-height: 1.8; background: #fff; padding-bottom: 80px; }
  header.site-header, .site-header, .page-title, h1:first-of-type { display: none !important; }

  /* ナビメニュー */
  .guide-menu { background: #fff9f0; border: 2px solid orange; border-radius: 15px; margin: 20px 15px; padding: 15px; }
  .guide-menu-title { font-weight: bold; color: orange; text-align: center; margin-bottom: 10px; font-size: 16px; }
  .guide-menu ul { list-style: none; padding: 0; margin: 0; display: grid; grid-template-columns: 1fr; gap: 8px; }
  .guide-menu a { text-decoration: none; color: #555; font-size: 14px; display: block; padding: 5px; border-bottom: 1px dashed #ffd8a8; }
  .guide-menu a::before { content: "🐾"; margin-right: 8px; }

  /* コンテンツ */
  .guide-section { padding: 30px 15px 10px; scroll-margin-top: 20px; }
  .guide-h2 { background: linear-gradient(to right, orange, #ffcc00); color: white; padding: 12px 15px; border-radius: 8px; font-size: 18px; margin-bottom: 20px; box-shadow: 0 4px 10px rgba(255,165,0,0.2); }
  .guide-h3 { border-left: 5px solid orange; padding-left: 10px; margin: 25px 0 10px; font-size: 17px; font-weight: bold; color: #444; }
  
  /* カード形式の解説 */
  .info-card { background: #fefefe; border: 1px solid #eee; border-radius: 12px; padding: 15px; margin: 15px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
  .price-tag { display: inline-block; background: #fff5f5; color: #e03131; padding: 2px 10px; border-radius: 5px; font-weight: bold; font-size: 14px; margin-bottom: 10px; }

  /* 都道府県ボタン */
  .region-title { background: #eee; padding: 5px 10px; font-size: 14px; font-weight: bold; margin-top: 15px; border-radius: 5px; }
  .pref-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; margin-top: 10px; }
  .pref-btn { background: white; border: 1px solid #ddd; padding: 8px; border-radius: 5px; text-align: center; text-decoration: none; color: #333; font-size: 12px; }
  .pref-btn:active { background: orange; color: white; border-color: orange; }

  /* 年間スケジュール表 */
  .schedule-table { width: 100%; border-collapse: collapse; margin-top: 15px; font-size: 13px; }
  .schedule-table th, .schedule-table td { border: 1px solid #ddd; padding: 10px 5px; text-align: center; }
  .schedule-table th { background: #fff4e6; color: #d9480f; }
</style>

<div class="guide-body">
  <div style="text-align:center; padding: 30px 0 10px;">
    <h1 style="font-size: 24px; color: orange; margin-bottom: 5px;">🔰 はじめての飼い主さんガイド</h1>
    <p style="font-size: 13px; color: #888;">愛犬を守るために必要な手続きと健康管理</p>
  </div>

  <nav class="guide-menu">
    <div class="guide-menu-title">目次（タップで移動）</div>
    <ul>
      <li><a href="#microchip">マイクロチップの装着・登録</a></li>
      <li><a href="#vaccine">健康診断と混合ワクチン</a></li>
      <li><a href="#rabies">狂犬病予防接種とハガキ</a></li>
      <li><a href="#registration">自治体への登録（日本地図から探す）</a></li>
      <li><a href="#annual">年間の予防スケジュール</a></li>
    </ul>
  </nav>

  <section id="microchip" class="guide-section">
    <h2 class="guide-h2">マイクロチップの装着・登録</h2>
    <p>マイクロチップは、ワンちゃんが迷子になったり、災害ではぐれた際に「誰の犬か」を証明する大切な身分証明書です。</p>
    <div class="info-card">
      <div class="price-tag">費用の目安：3,000円〜10,000円程度</div>
      <p><strong>保護犬を迎えた場合：</strong><br>
      前の飼い主さんや保護団体から引き継いだ後、速やかに**動物病院での装着（未装着の場合）と、環境省への登録変更**が必要です。</p>
      <p style="font-size: 13px; color: #666;">※別途、登録手数料（オンラインなら数百円、ハガキなら千円程度）がかかります。</p>
    </div>
  </section>

  <section id="vaccine" class="guide-section">
    <h2 class="guide-h2">健康診断と混合ワクチン</h2>
    <p>家に来て落ち着いたら、まずは動物病院へ。便検査（寄生虫確認）や触診を受けましょう。</p>
    
    <div class="info-card">
      <h3 class="guide-h3" style="margin-top:0;">混合ワクチンとは？</h3>
      <p>狂犬病ワクチン（法律）とは異なり、**「ワンちゃん同士で感染する恐ろしい病気」**を予防する任意のワクチンです。</p>
      <ul>
        <li><strong>なぜ必要？</strong>：パルボウイルスやジステンパーなど、致死率の高い病気から命を守るためです。</li>
        <li><strong>社会のマナー</strong>：ドッグラン、ペットホテル、トリミングサロンなどの利用時に、**「混合ワクチン接種証明書」**の提示が必須となることがほとんどです。</li>
      </ul>
      <div class="price-tag">費用の目安：5,000円〜10,000円（5種〜10種など）</div>
    </div>
  </section>

  <section id="rabies" class="guide-section">
    <h2 class="guide-h2">狂犬病予防接種</h2>
    <p>法律で定められた**「飼い主の義務」**です。毎年1回必ず受けましょう。</p>
    <div class="info-card">
      <p>毎年春頃に、市町村から届く**「通知ハガキ」**を動物病院へ持参してください。</p>
      <p><strong>【重要】他県の病院で受ける場合：</strong><br>
      他県のかかりつけ医などで接種した場合、病院で発行される「接種証明書」を持って、**自分の住んでいる自治体の窓口で別途「注射済票」の手続き**を行う必要があります。これを忘れると「未接種」扱いになるので注意しましょう。</p>
    </div>
  </section>

  <section id="registration" class="guide-section">
    <h2 class="guide-h2">自治体への登録（地域から探す）</h2>
    <p>ワンちゃんを飼い始めたら、お住まいの市区町村への登録が必要です。手続き窓口を探すためのガイドです。</p>
    
    [attachment_0](attachment)
    
    <div class="info-card">
      <p style="font-size: 13px;">※以下の都道府県名を選択すると、各自治体の登録案内（または検索ページ）へ移動します。</p>
      
      <div class="region-title">関東</div>
      <div class="pref-grid">
        <a href="https://www.google.com/search?q=東京都+犬+登録" class="pref-btn">東京都</a>
        <a href="https://www.google.com/search?q=神奈川県+犬+登録" class="pref-btn">神奈川県</a>
        <a href="https://www.google.com/search?q=埼玉県+犬+登録" class="pref-btn">埼玉県</a>
        <a href="https://www.google.com/search?q=千葉県+犬+登録" class="pref-btn">千葉県</a>
        <a href="https://www.google.com/search?q=茨城県+犬+登録" class="pref-btn">茨城県</a>
        <a href="https://www.google.com/search?q=栃木県+犬+登録" class="pref-btn">栃木県</a>
        <a href="https://www.google.com/search?q=群馬県+犬+登録" class="pref-btn">群馬県</a>
      </div>

      <div class="region-title">その他の地域（全国リスト）</div>
      <p style="font-size: 13px; margin-top:10px;">全国の自治体の窓口や、詳しい手続きの流れは以下の厚生労働省の公式ページから確認できます。</p>
      <a href="https://www.mhlw.go.jp/stf/seisakunitsuite/bunya/0000139450.html" class="pref-btn" style="width:100%; display:block; background:orange; color:white; border:none; font-weight:bold;">厚生労働省：犬の登録手続き一覧</a>
    </div>
  </section>

  <section id="annual" class="guide-section">
    <h2 class="guide-h2">年間の予防スケジュール</h2>
    <p>1年を通じて、愛犬を健康トラブルから守るためのスケジュールです。</p>
    
    <table class="schedule-table">
      <thead>
        <tr>
          <th>項目</th>
          <th>時期</th>
          <th>目的</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>狂犬病予防</td>
          <td>4〜6月</td>
          <td>法律義務の予防</td>
        </tr>
        <tr>
          <td>フィラリア薬</td>
          <td>5〜12月</td>
          <td>蚊が媒介する寄生虫予防</td>
        </tr>
        <tr>
          <td>混合ワクチン</td>
          <td>年1回</td>
          <td>感染症の予防（社会マナー）</td>
        </tr>
        <tr>
          <td>ノミ・ダニ薬</td>
          <td>通年</td>
          <td>マダニ等の寄生虫予防</td>
        </tr>
      </tbody>
    </table>
  </section>

  <div style="text-align: center; margin-top: 50px;">
    <a href="{{ '/' | relative_url }}" style="color: orange; font-weight: bold; text-decoration: none;">← ホームに戻る</a>
  </div>
</div>
