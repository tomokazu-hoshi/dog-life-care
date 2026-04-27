---
layout: default
title: 都道府県を選択
permalink: /registration-search/
---

<style>
  /* 1. 不要なタイトルを非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* 2. オレンジのヘッダー */
  .custom-header { 
    background: white; padding: 18px 0; text-align: center; border-bottom: 3px solid orange; 
    display: flex; align-items: center; justify-content: center; width: 100%;
  }
  .custom-logo { font-size: 22px; margin-right: 8px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  /* 3. コンテナ（横幅をiPhoneに最適化） */
  .container { width: 94%; max-width: 500px; margin: 0 auto; padding: 20px 0 60px; }
  
  .step-label { font-size: 13px; color: #888; text-align: center; margin-bottom: 20px; }
  .step-label b { color: orange; }

  /* 4. 地方ごとのセクション */
  .region-section { margin-bottom: 25px; }
  .region-name { 
    font-size: 16px; font-weight: bold; color: #555; 
    padding: 5px 12px; border-left: 4px solid orange; background: #eee; 
    margin-bottom: 12px; border-radius: 0 5px 5px 0;
  }

  /* 5. 都道府県ボタン（3列グリッド） */
  .pref-grid { 
    display: grid; 
    grid-template-columns: repeat(3, 1fr); 
    gap: 10px; 
  }

  .pref-btn { 
    background: white; border: 1px solid #ddd; border-radius: 10px; 
    padding: 15px 5px; text-align: center; text-decoration: none; 
    color: #333; font-size: 14px; font-weight: bold;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    transition: 0.2s;
  }
  .pref-btn:active { background: #fff9f0; border-color: orange; color: orange; transform: scale(0.95); }
</style>

<div class="custom-header">
  <span class="custom-logo">🗺️</span>
  <div class="custom-title">自治体検索</div>
</div>

<div class="container">
  <div class="step-label">STEP 2：<b>都道府県を選択</b>してください</div>

  <div class="region-section">
    <div class="region-name">北海道・東北</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/hokkaido/' | relative_url }}" class="pref-btn">北海道</a>
      <a href="{{ '/registration-search/aomori/' | relative_url }}" class="pref-btn">青森</a>
      <a href="{{ '/registration-search/iwate/' | relative_url }}" class="pref-btn">岩手</a>
      <a href="{{ '/registration-search/miyagi/' | relative_url }}" class="pref-btn">宮城</a>
      <a href="{{ '/registration-search/akita/' | relative_url }}" class="pref-btn">秋田</a>
      <a href="{{ '/registration-search/yamagata/' | relative_url }}" class="pref-btn">山形</a>
      <a href="{{ '/registration-search/fukushima/' | relative_url }}" class="pref-btn">福島</a>
    </div>
  </div>

  <div class="region-section">
    <div class="region-name">関東</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/tokyo/' | relative_url }}" class="pref-btn">東京</a>
      <a href="{{ '/registration-search/kanagawa/' | relative_url }}" class="pref-btn">神奈川</a>
      <a href="{{ '/registration-search/saitama/' | relative_url }}" class="pref-btn">埼玉</a>
      <a href="{{ '/registration-search/chiba/' | relative_url }}" class="pref-btn">千葉</a>
      <a href="{{ '/registration-search/ibaraki/' | relative_url }}" class="pref-btn">茨城</a>
      <a href="{{ '/registration-search/tochigi/' | relative_url }}" class="pref-btn">栃木</a>
      <a href="{{ '/registration-search/gunma/' | relative_url }}" class="pref-btn">群馬</a>
    </div>
  </div>

  <div class="region-section">
    <div class="region-name">中部</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/niigata/' | relative_url }}" class="pref-btn">新潟</a>
      <a href="{{ '/registration-search/toyama/' | relative_url }}" class="pref-btn">富山</a>
      <a href="{{ '/registration-search/ishikawa/' | relative_url }}" class="pref-btn">石川</a>
      <a href="{{ '/registration-search/fukui/' | relative_url }}" class="pref-btn">福井</a>
      <a href="{{ '/registration-search/yamanashi/' | relative_url }}" class="pref-btn">山梨</a>
      <a href="{{ '/registration-search/nagano/' | relative_url }}" class="pref-btn">長野</a>
      <a href="{{ '/registration-search/gifu/' | relative_url }}" class="pref-btn">岐阜</a>
      <a href="{{ '/registration-search/shizuoka/' | relative_url }}" class="pref-btn">静岡</a>
      <a href="{{ '/registration-search/aichi/' | relative_url }}" class="pref-btn">愛知</a>
    </div>
  </div>

  <div class="region-section">
    <div class="region-name">近畿</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/mie/' | relative_url }}" class="pref-btn">三重</a>
      <a href="{{ '/registration-search/shiga/' | relative_url }}" class="pref-btn">滋賀</a>
      <a href="{{ '/registration-search/kyoto/' | relative_url }}" class="pref-btn">京都</a>
      <a href="{{ '/registration-search/osaka/' | relative_url }}" class="pref-btn">大阪</a>
      <a href="{{ '/registration-search/hyogo/' | relative_url }}" class="pref-btn">兵庫</a>
      <a href="{{ '/registration-search/nara/' | relative_url }}" class="pref-btn">奈良</a>
      <a href="{{ '/registration-search/wakayama/' | relative_url }}" class="pref-btn">和歌山</a>
    </div>
  </div>

  <div class="region-section">
    <div class="region-name">中国・四国</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/tottori/' | relative_url }}" class="pref-btn">鳥取</a>
      <a href="{{ '/registration-search/shimane/' | relative_url }}" class="pref-btn">島根</a>
      <a href="{{ '/registration-search/okayama/' | relative_url }}" class="pref-btn">岡山</a>
      <a href="{{ '/registration-search/hiroshima/' | relative_url }}" class="pref-btn">広島</a>
      <a href="{{ '/registration-search/yamaguchi/' | relative_url }}" class="pref-btn">山口</a>
      <a href="{{ '/registration-search/tokushima/' | relative_url }}" class="pref-btn">徳島</a>
      <a href="{{ '/registration-search/kagawa/' | relative_url }}" class="pref-btn">香川</a>
      <a href="{{ '/registration-search/ehime/' | relative_url }}" class="pref-btn">愛媛</a>
      <a href="{{ '/registration-search/kochi/' | relative_url }}" class="pref-btn">高知</a>
    </div>
  </div>

  <div class="region-section">
    <div class="region-name">九州・沖縄</div>
    <div class="pref-grid">
      <a href="{{ '/registration-search/fukuoka/' | relative_url }}" class="pref-btn">福岡</a>
      <a href="{{ '/registration-search/saga/' | relative_url }}" class="pref-btn">佐賀</a>
      <a href="{{ '/registration-search/nagasaki/' | relative_url }}" class="pref-btn">長崎</a>
      <a href="{{ '/registration-search/kumamoto/' | relative_url }}" class="pref-btn">熊本</a>
      <a href="{{ '/registration-search/oita/' | relative_url }}" class="pref-btn">大分</a>
      <a href="{{ '/registration-search/miyazaki/' | relative_url }}" class="pref-btn">宮崎</a>
      <a href="{{ '/registration-search/kagoshima/' | relative_url }}" class="pref-btn">鹿児島</a>
      <a href="{{ '/registration-search/okinawa/' | relative_url }}" class="pref-btn">沖縄</a>
    </div>
  </div>

  <div style="text-align: center; margin-top: 40px;">
    <a href="{{ '/beginners-guide/' | relative_url }}" style="color: #888; font-size: 14px; text-decoration: none;">← ガイドに戻る</a>
  </div>
</div>
