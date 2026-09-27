# japan-mab-youth

活動報告の作成
①写真のアップロード
・japan-mab-youth/imagesに、イベントごとにファイルを作成し、写真をアップロードする。
・イベントごとにファイルを作成する。

②活動報告へのイベント追加
・index.htmlの「<!-- 活動報告 -->」を検索する。
・<div class="cards" id="activity-cards">以降に新たなイベントを追加する。
---テンプレート---
<div class="card" data-region="domestic/international" data-ecopark="yes/no" data-format="host/group/individual" data-year="2025/2026" data-id="name" onclick="showDetail('name')">
  <img src="link" alt="">
  <div class="card-body">
    <span class="card-tag lang-ja">🇯🇵 国内/🌍 国外</span><span class="card-tag lang-en">🇯🇵 Domestic/🌍 International</span>
    <span class="card-year">year.month.day~day</span>
    <h3 class="lang-ja">名前</h3>
    <h3 class="lang-en">name</h3>
    <p class="lang-ja">1文説明。</p>
    <p class="lang-en">one-sentence description</p>
  </div>
</div>
----------------

③活動報告の詳細ページの作成
・index.htmlの「// --- 活動詳細 ---」を検索する。
・「const activityDetails = {」以下に、新たなイベントを追加する。
---テンプレート---
'name': {
titleJa: '名前（場所）',
titleEn: 'name (location)',
photos: ["写真パス","写真パス","写真パス"
],
tagsHtml: '<span class="card-tag lang-ja">🇯🇵 国内/🌍 国外</span><span class="card-tag lang-en">🇯🇵 Domestic/🌍 International</span><span class="card-tag lang-ja">🍃 ユネスコエコパーク</span><span class="card-tag lang-en">🍃 UNESCO Eco Park</span><span class="card-year">year.month.day~day</span>',
bodyJa: `
<p><strong>概要</strong>本文</p>
<p><strong>目的</strong>本文</p>
<p><strong>内容</strong>本文</p>
<p><strong>成果・学び</strong>本文。</p>
`,
bodyEn: `
<p><strong>Overview</strong>Write here.</p>
<p><strong>Background / Purpose</strong>Write here.</p>
<p><strong>Details</strong>Write here.</p>
<p><strong>Outcomes / Takeaways</strong>Write here.</p>
`
},
----------------
