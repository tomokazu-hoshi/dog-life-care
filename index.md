---
layout: default
title: ワンライフ・ナビ
---

<style>
  /* 全体設定：iPhoneで見やすいフォント */
  body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; background-color: #f6f8fa; color: #333; margin: 0; }
  
  /* セクションタイトル（「カテゴリーから探す」など）：オレンジ下線付き */
  .custom-section-title { text-align: center; font-size: 22px; font-weight: bold; margin-top: 40px; margin-bottom: 25px; position: relative; padding-bottom: 12px; color: #333; }
  .custom-section-title::after { content: ""; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 45px; height: 3px; background-color: orange; border-radius: 2px; }

  /* 3x3 グリッドレイアウト */
  .custom-category-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; max-width: 350px; margin: 0 auto; padding: 0 10px; }

  /* カテゴリーカード（リンク）：白背景、角丸、シャドウ */
  .custom-category-card { background-color: white; border-radius: 12px; box-shadow: 0 3px 6px rgba(0,0,0,0.1); text-align: center; padding: 18px 5px; text-decoration: none; color: #333; display: flex; flex-direction: column; align-items: center; }
  
  /* カード内のアイコン（SVG、またはPNG）：オレンジ色にする設定 */
  .custom-card-icon { width: 40px; height: 40px; margin-bottom: 8px; font-size: 32px; color: orange; /* 暫定的にSVGやWebフォントアイコンを想定 */ }
  
  /* カード内のテキスト（「しつけ」など） */
  .custom-card-title { font-size: 13px; font-weight: bold; line-height: 1.2; }

  /* --- 以下のCSSは、PNG画像アイコンを持っている場合に必要 --- */
  /* 各アイコンのPNG画像へのパス（ assets/images/icons/ にPNG画像を置いたと仮定）
  .icon-training { background-image: url("https://your-repository.github.io/dog-life-care/assets/images/icons/icon-training.png"); background-size: contain; background-repeat: no-repeat; background-position: center; width: 40px; height: 40px; margin-bottom: 8px; }
  .icon-diet { background-image: url("https://your-repository.github.io/dog-life-care/assets/images/icons/icon-diet.png"); /* 同上 */ }
  ...他のアイコンも同様に設定...
  */
  /* PNGアイコンを使う場合は、HTML内のアイコン（SVG）を消して、クラス（icon-trainingなど）を追加する */
</style>

<div class="custom-section-title">カテゴリーから探す</div>

<div class="custom-category-grid">
  
  <a href="{{ '/training/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🎓</div> <div class="custom-card-title">しつけ</div>
  </a>

  <a href="{{ '/diet/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🍴</div> <div class="custom-card-title">食事</div>
  </a>

  <a href="{{ '/health/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🩺</div> <div class="custom-card-title">健康・医療</div>
  </a>

  <a href="{{ '/care/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🚿</div> <div class="custom-card-title">お手入れ</div>
  </a>

  <a href="{{ '/dog-search/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">📖</div> <div class="custom-card-title">犬種図鑑</div>
  </a>

  <a href="{{ '/faq/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">💬</div> <div class="custom-card-title">FAQ</div>
  </a>

  <a href="{{ '/outing/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">🐾</div> <div class="custom-card-title">お出かけ</div>
  </a>

  <a href="{{ '/health-check/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">⌛</div> <div class="custom-card-title">年齢診断</div>
  </a>

  <a href="{{ '/others/' | relative_url }}" class="custom-category-card">
    <div class="custom-card-icon">➕</div> <div class="custom-card-title">その他</div>
  </a>

</div>
