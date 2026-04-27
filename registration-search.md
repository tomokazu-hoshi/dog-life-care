---
layout: default
title: 自治体窓口検索
permalink: /registration-search/
---

<style>
  /* 1. 不要なタイトルを非表示 */
  header.site-header, .site-header, .page-title, h1:first-of-type, .main-content h1:first-child { 
    display: none !important; 
  }

  /* 2. 全体の基本設定 */
  body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; background-color: #f6f8fa; margin: 0; padding: 0; color: #333; }
  
  /* 3. オレンジのヘッダー */
  .custom-header { 
    background: white; padding: 20px 0; text-align: center; border-bottom: 3px solid orange; 
    display: flex; align-items: center; justify-content: center; 
  }
  .custom-logo { font-size: 24px; margin-right: 10px; }
  .custom-title { font-size: 20px; font-weight: bold; color: orange; margin: 0; }

  /* 4. メインコンテナ */
  .search-container { 
    width: 92%; max-width: 400px; margin: 0 auto; padding: 40px 0 60px; text-align: center; 
  }

  /* 5. 説明テキスト */
  .search-intro { font-size: 15px; line-height: 1.6; color: #666; margin-bottom: 30px; }
  .search-intro b { color: #333; }

  /* 6. 【1段階目】メインボタン */
  .step1-button { 
    display: flex; align-items: center; justify-content: center;
    background: linear-gradient(135deg, #ff9d00, #ffbb00);
    color: white !important; text-decoration: none;
    padding: 25px 15px; border-radius: 20px;
    font-size: 19px; font-weight: bold;
    box-shadow: 0 6px 15px rgba(255,157,0,0.3);
    transition: 0.2s;
    border: none; width: 100%; cursor: pointer;
  }
  .step1-button:active { transform: scale(0.98); box-shadow: 0 2px 5px rgba(255,157,0,0.3); }
  .btn-icon { font-size: 26px; margin-right: 12px; }

  /* 7. 補足情報 */
  .search-tip { 
    margin-top: 40px; background: #fff; padding: 20px; border-radius: 15px; 
    border: 1px dashed #ccc; font-size: 13px; color: #888; text-align: left;
  }
</style>

<div class="custom-header">
  <span class="custom-logo">🔍</span>
  <div class="custom-title">全国自治体 登録窓口検索</div>
</div>

<div class="search-container">
  
  <div class="search-intro">
    ワンちゃんを迎えたら30日以内に、<br>
    <b>お住まいの市区町村</b>への登録が必要です。<br>
    手続きを行う窓口をここから探せます。
  </div>

  <a href="#step2" class="step1-button">
    <span class="btn-icon">🗺️</span>各自治体の検索はこちら
  </a>

  <div class="search-tip">
    <strong>💡 手続きについて：</strong><br>
    登録が完了すると「鑑札（かんさつ）」が交付されます。これはワンちゃんの身分証明書として、首輪などに常に付けておくことが法律で義務付けられています。
  </div>

  <div style="margin-top: 40px;">
    <a href="javascript:history.back()" style="color: #888; font-size: 14px; text-decoration: none;">← 前の画面に戻る</a>
  </div>

</div>
