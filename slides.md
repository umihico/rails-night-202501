---
# You can also start simply with 'default'
# theme: seriph
theme: apple-basic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: "Rails Night: 急成長スタートアップの本番コードを解剖する"
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
# class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# layout: intro-image
# image: background.png
layout: intro
colorSchema: auto
---

<img src="/assets/connpass.png" class="w-full px-10 mb-5">

# Railsと共に歩む泥道
## ~プレーリーカードの本当は知ってほしくない、言いたくない開発事情~

### Umihiko Iwasa

<style>
h2 {
  font-size: 1em !important;
  line-height: 1.5em !important;
}
.slidev-layout{
  background-color: #499DA2;
  background-image: url("/assets/logo.png");
  background-repeat: no-repeat;
  background-position: right 5% bottom 5%;
  background-size: 25%;
}
</style>

---
layout: intro
transition: slide-left

# transition: fade-out
---

## 自己紹介

<p></p>

# 岩佐 <span v-mark.circle.orange="1">海</span>彦

<p></p>

### Work
株式会社スタジオプレーリー　<span v-click="4" v-mark.orange="4">※プレーリーカードの会社</span>
### Role
<span v-mark.orange="5">フルスタックエンジニア、バックエンドエンジニアマネージャー</span>
### Love
<span v-mark.orange="6">Ruby on Rails</span>、AWS、Terraform、Next.js、TypeScript
### Web
<span>https://github.com/umihico/rails-night-202501 (本資料・Slidev)</span>
<br/>
<span>https://my.prairie.cards/u/umihico (プレーリーカード)</span>

<p v-click="2" class="absolute transform rotate-8" style="left: 610px;top: 210px;">私</p>
<arrow v-click="2" x1="600" y1="250" x2="750" y2="270" color="#FFF" width="2" arrowSize="1" />

<p v-click="3" class="absolute transform" style="left: 730px;top: 440px;">誰かの頭</p>
<arrow v-click="3" x1="800" y1="450" x2="840" y2="410" color="#FFF" width="2" arrowSize="1" />

<style>
h1 {
  font-size: 2em !important;
}
.slidev-layout{
  background-color: #499DA2;
  background-image: url("/assets/umihiko_iwasa.jpg");
  background-repeat: no-repeat;
  background-position: right 5% bottom 50%;
  background-size: 25%;
}
</style>

<!--
皆さんからはうみさん、うみちゃんと短く呼んでもらっています。


写真はいつもこの、私と、誰かの頭のツーショットの写真を使っています。

スタジオプレーリーというところで働いています。プレーリーカードを作っている会社です。

フルスタックWEBエンジニア、バックエンドエンジニアマネージャーとして働いています。

好きなものは色々ありますが、Railsが好きです。

このURLがプレーリーカードの私のプロフィールページになっています。スポンサーLTをということで、少しこのプレーリーカードについて紹介させてください。
-->

---
transition: slide-left
---

<style>

h1 {
  font-size: 2em !important;
}
.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# プレーリーカード is 何

<div class="flex w-full mt-5">
  <img src="/assets/iphone-profile.png" class="h-100 object-cover mt-5">
  <img src="/assets/iphone-profile2.png" class="h-100 object-cover mx-6 mt-5">
  <img src="/assets/demo.gif" class="h-60 object-cover mt-40 ms-10">
</div>
<div v-click=1 class="fixed left-130 top-20 text-xl">
<h2 class="mb-2">👉デジタル名刺</h2>
<li><span>アプリもカメラも不要</span></li>
<li><span>エコ＆名刺切れの心配なし</span></li>
<li><span>各SNSや画像・URL・コンテンツを掲載可</span></li>
<li><span>完全オリジナルデザイン可・木材素材も</span></li>
</div>

<!--
プレーリーカードとはデジタル名刺です。

普通の紙の名刺とは違います。

お相手のスマートフォンを、カードの上にかざしてもらいます。

そうすると、ブラウザーが開きます。そして、自分のプロフィールが表示される。そういうアイテムになっています。

今見てもらっている通り、相手はアプリをインストールしたり、カメラを起動したりしてもらう必要はありません。

プレーリーカードはこの１枚をずっと使うことができるので、環境にも優しいエコなアイテムになっています。また、さらに環境に配慮した、木の素材で作られたプレーリーカードも販売しています。

プロフィールの内容は通常の名刺にある肩書や電話番号、メールアドレスはもちろんあります。

加えて、Xやインスタグラム、LinkedInなど好きなソーシャルメディアのリンクをのせることができます。

プレーリーカードはその下に好きなコンテンツを載せることができます。例えばエンジニアなら、ポートフォリオサイトなど。営業マンなら会社の資料や、日程調整ツールなどです。

私が一番使っているのは、エンジニア同士のミートアップなどカジュアルな機会です。どのソーシャルメディアをやっているか確かめたり、アカウント名で検索してもらったり、そういう手間がなくつながることができるようになります。

また、初対面から、会話が盛り上がる共通点が見つかるまでには、時間がかかるのが普通だと思います。ですが、プレーリーカードはテキストやコンテンツで自己紹介ができているので、相手が気になるものがあれば拾ってくれます。そうすることで、今までは本当は共通点があるのに、うまく見つけられないまま会話が終わってしまった、そういったことが減らせるようになります。
-->

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# 早速、Rails Stats？

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# Quiz: 現在のプレーリーカードの開発チームの規模は？

<p class="h-3"></p>

# 1. １人
# 2. ３人
# 3. ５人
# 4. ７人
# 5. １０人

---
transition: slide-left
---

<style>
.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# 弊社の人員構成

<p class="h-3"></p>

<li>エンジニアもできる共同代表 1名</li>
<li>デザインもできる共同代表 1名</li>
<li>COO 兼 CFO 兼 法人事業責任者 1名</li>
<li>個人事業責任者 1名</li>
<li>法人営業 1名</li>
<li>エンジニア(私) 1名<span v-click=1 v-mark.orange=1> but 産休</span></li>

上記に加えインターンや業務委託で梱包発送・PdM・営業顧問・採用担当・デザイナー・マーケターの方々！

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# Quiz: 現在のプレーリーカードの開発チームの規模は？

<p class="h-3"></p>

<h1><span v-mark.orange.circle=1>1. １人</span></h1>

# 2. ３人
# 3. ５人
# 4. ７人
# 5. １０人

<img v-click=1 src="/assets/only-daichi.png" class="h-30 object-cover">

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# サービス構成

- Rails × App Runnerでプロフィールページ
- Next.js × Amplifyでカードデザイン作成ページ
  - [EMConf](https://2025.emconf.jp/posts/ticket-infomation/)用の各カードはこちらで作りました
- Shopifyでランディングページ
- AWS、GCPはTerraformで管理
- 開発量はRails > Next.js > Shopify > AWS > others

<img src="/assets/infra/current.png" class="h-145 fixed top-0 right-0">

<!--

-->

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# リリース当時

※私のジョイン前
<li v-click=1><a href="https://prtimes.jp/main/html/rd/p/000000002.000063728.html">PR Times(2023-02-07)</a></li>
<img v-click=[1] src="/assets/screenshots/prtimes.png" class="h-full fixed right-0 top-0">
<li v-click=2><a href="https://github.com/prairie-card/prairie_card/pulls?q=closed%3A%3C%3D2023-02-07+">プルリク8個(!)</a></li>
<img v-click=[2] src="/assets/screenshots/pr8.png" class="h-full fixed right-0 top-0">
<li v-click=3>モデル18個、テスト0個(!)</li>
<img v-click=3 src="/assets/rails_stats/release.png" class="w-150 fixed -right-5 top-30">

<p class="h-3"></p>

<div v-click=4>
<h2>感想</h2>
これの体現じゃん
<li>MVP</li>
<li>「まず売れ、後で作れ」</li>
<li>"Done is better than perfect"</li>
<li>"If you are not embarrassed by the first version of your product, you’ve launched too late."</li>
</div>

<span v-click=5>スタートアップのやるべきムーブを地でやっていてすごい</span>
<span v-click=6>（全力のヨイショ）</span>

<!--
+----------------------+--------+--------+---------+---------+-----+-------+
| Name                 |  Lines |    LOC | Classes | Methods | M/C | LOC/M |
+----------------------+--------+--------+---------+---------+-----+-------+
| Controllers          |   1352 |    973 |      22 |      65 |   2 |    12 |
| Helpers              |      4 |      4 |       0 |       0 |   0 |     0 |
| Models               |    893 |    393 |      18 |      20 |   1 |    17 |
| Mailers              |     60 |     41 |       4 |       3 |   0 |    11 |
| JavaScripts          |  27555 |  24782 |       0 |    1388 |   0 |    15 |
| JavaScript           |     33 |      0 |       0 |       0 |   0 |     0 |
| Libraries            |    347 |    293 |       4 |       3 |   0 |    95 |
+----------------------+--------+--------+---------+---------+-----+-------+
| Total                |  30244 |  26486 |      48 |    1479 |  30 |    15 |
+----------------------+--------+--------+---------+---------+-----+-------+
  Code LOC: 26486     Test LOC: 0     Code to Test Ratio: 1:0.0
-->
---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# リリース１周年記念

※少し首を突っ込み始めるワイ
<li v-click=1><a href="https://prtimes.jp/main/html/rd/p/000000013.000063728.html">PR Times(2024-02-07)</a></li>
<img v-click=[1] src="/assets/screenshots/prtimes2.png" class="h-full fixed right-0 top-0">
<li v-click=2><a href="https://github.com/prairie-card/prairie_card/pulls?q=closed%3A%3C%3D2023-02-07+">プルリク996個!</a></li>
<img v-click=[2] src="/assets/screenshots/pr996.png" class="h-full fixed right-0 top-0">
<li v-click=3>モデル63個、テストレシオ0.1</li>
<img v-click=3 src="/assets/rails_stats/oneyear.png" class="w-150 fixed -right-5 top-30">

<p class="h-40"></p>

<div v-click=4>
<h2>感想</h2>
<li>ファンミーティング最高だったなぁ</li>
<li>テストレシオ低いのは外部JS直接貼り付けたせいでコード量多いから。きっとそう</li>
</div>

<!--
+----------------------+--------+--------+---------+---------+-----+-------+
| Name                 |  Lines |    LOC | Classes | Methods | M/C | LOC/M |
+----------------------+--------+--------+---------+---------+-----+-------+
| Controllers          |   5026 |   4034 |      81 |     269 |   3 |    12 |
| Helpers              |     11 |      7 |       0 |       1 |   0 |     5 |
| Models               |   3342 |   1462 |      63 |      89 |   1 |    14 |
| Mailers              |    112 |     72 |       6 |       6 |   1 |    10 |
| Channels             |     51 |     38 |       3 |       3 |   1 |    10 |
| JavaScripts          |  27550 |  24774 |       0 |    1387 |   0 |    15 |
| Libraries            |   1207 |    911 |      20 |       7 |   0 |   128 |
| Controller specs     |     44 |     34 |       1 |       0 |   0 |     0 |
| Lib specs            |     33 |     28 |       0 |       0 |   0 |     0 |
| Model specs          |   1077 |    766 |       2 |       2 |   1 |   381 |
| Request specs        |   3319 |   2834 |       3 |       3 |   1 |   942 |
+----------------------+--------+--------+---------+---------+-----+-------+
| Total                |  41772 |  34960 |     179 |    1767 |   9 |    17 |
+----------------------+--------+--------+---------+---------+-----+-------+
  Code LOC: 31298     Test LOC: 3662     Code to Test Ratio: 1:0.1
-->

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# そして現在

<li v-click=1>プルリク2555個</li>
<img v-click=[1] src="/assets/screenshots/pr2555.png" class="h-full fixed right-0 top-0">
<li v-click=2>モデル88個、テストレシオ0.3</li>
<img v-click=2 src="/assets/rails_stats/now.png" class="w-150 fixed right-0 top-30">

<p class="h-60"></p>

<div v-click=3>
<h2>感想</h2>
<li>モデルあんまり増えてないなぁ。新機能より既存機能のUX改善が多くなってきた感覚</li>
</div>

<!--
+----------------------+--------+--------+---------+---------+-----+-------+
| Name                 |  Lines |    LOC | Classes | Methods | M/C | LOC/M |
+----------------------+--------+--------+---------+---------+-----+-------+
| Controllers          |   8047 |   6488 |     111 |     467 |   4 |    11 |
| Helpers              |    102 |     69 |       0 |      11 |   0 |     4 |
| Models               |   5739 |   2870 |      88 |     231 |   2 |    10 |
| Mailers              |    109 |     84 |       4 |       7 |   1 |    10 |
| Channels             |     60 |     42 |       3 |       3 |   1 |    12 |
| JavaScripts          |  27549 |  24772 |       0 |    1387 |   0 |    15 |
| JavaScript           |    188 |    172 |       0 |       0 |   0 |     0 |
| Libraries            |   1848 |   1392 |      29 |      11 |   0 |   124 |
| Controller specs     |    434 |    372 |       3 |       0 |   0 |     0 |
| Helper specs         |    111 |     88 |       0 |       0 |   0 |     0 |
| Lib specs            |     61 |     53 |       0 |       0 |   0 |     0 |
| Model specs          |   3809 |   2508 |       2 |       3 |   1 |   834 |
| Request specs        |   7192 |   6299 |       4 |       6 |   1 |  1047 |
| Service specs        |    155 |    145 |       0 |       0 |   0 |     0 |
+----------------------+--------+--------+---------+---------+-----+-------+
| Total                |  55404 |  45354 |     244 |    2126 |   8 |    19 |
+----------------------+--------+--------+---------+---------+-----+-------+
  Code LOC: 35889     Test LOC: 9465     Code to Test Ratio: 1:0.3
-->

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# プレーリーカードの光と闇のトーク①【Gemfile抜粋】

```ruby
ruby "3.2.4" # (´・ω・｀)ﾅﾆｺﾚ
gem "rails", "~> 6.1.4", ">= 6.1.4.6" # (´・ω・｀)ﾅﾆｺﾚ
gem "pg" # ポスグレで動いてます
gem "slim-rails" # viewをslimで書いてます
gem "discard" # 論理削除を使ってます
gem "sentry-ruby"; gem "sentry-rails" # エラー監視はSentry
gem 'apipie-rails' # Flutter用
gem "sendgrid-ruby" # メール送信用だが細かいオプションがgem未対応なので直接API叩いている
gem "cloudinary" # 画像の合成などで相当お世話になっているやつ
gem "lograge" # ログをJSONにしてBQに送るため
gem "rails_admin" # 管理画面
gem "cancancan" # 権限統制（法人向け）かつコントローラーをスッキリ（させたかった）
gem "data_migrate" # データマイグレーション
gem "audited" # ログ
gem "vcr" # テストはなるべくリアルなレスポンスを使う
```

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# プレーリーカードの光と闇のトーク②
# 【コードリーディングネタ】

<p class="h-1"></p>

- ユーザーの全行動を収集するデータ分析基盤(lograge -> Cloudwatch -> Github Actions -> BigQuery)
- 現物のカード(NFC)との戦い　書き込み＆ロックを行う配送作業用ページ
- 「個人転生」と呼んでいるスクリプトで、イベント等の際には個人ユーザーを一括大量作成
- カードのURLからプロフィールが表示されるまでの条件分岐や工夫
- 特許まで取りにいった「メールで保存」機能
- コテコテJS、ゴリゴリcanvasで書いた法人向け社員名付きカードデザイン一括生成機能
- 現在（片山が）開発中の新機能

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# We are hiring!

<p class="h-1"></p>

- 今の状態
  - bizがやりたいことが毎週10個増える
  - 開発がやりたいことが毎週10個増える
  - でも実現できるのは毎週半分もないくらい → 辛い！もったいない！

[採用ページ👉https://my.prairie.cards/u/prairie_recruit](https://my.prairie.cards/u/prairie_recruit)


<p class="h-3"></p>

<div v-click=1>
<div class="fixed bottom-10 right-5 text-3xl">Thank you!</div>
<img src="/assets/logo.png" class="fixed bottom-20 -right-40 w-60 pb-2">
</div>
