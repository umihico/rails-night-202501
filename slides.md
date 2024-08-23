---
# You can also start simply with 'default'
# theme: seriph
theme: apple-basic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: "Agile Infrastructure: Prairie Card's AWS Strategy for Dynamic Growth"
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

## Agile Infrastructure:
## Prairie Card's AWS Strategy for Dynamic Growth

### Umihiko Iwasa

<!-- 
# Agile Infrastructure:

Prairie Card's AWS Strategy for Dynamic Growth

<div class="absolute bottom-10">
  <span class="font-700">
    Umihiko Iwasa
  </span>
</div> -->


<style>
h2 {
  font-size: 1.9em !important;
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

<!--
プレーリーカードのスポンサーLTをさせていただきます。

アジャイルインフラストラクチャというタイトルでプレーリーカードがどのようにAWSを活用しているか、紹介させていただきます。
-->

---
layout: intro
# transition: slide-left
transition: fade-out
---

## Who is this speaker?

<p></p>

# <span v-mark.circle.orange="1">Umi</span>hiko Iwasa

<p></p>

### Work
Studio Prairie Inc. <span v-click="4" v-mark.orange="4">a.k.a. Prairie Card's company</span>
### Role
<span v-mark.orange="5">Full Stack Web Developer, Backend Engineer Manager</span>
### Love
<span v-mark.circle.orange="6">AWS</span><span v-click=[0,6]>, Terraform, Ruby on Rails, Next.js, TypeScript</span>
### Web
<span>https://my.prairie.cards/u/umihico</span>

<p v-click="7" class="absolute transform rotate-7" style="left: 400px;top: 460px;">Prairie Card</p>
<arrow v-click="7" x1="500" y1="510" x2="350" y2="490" color="#FFF" width="2" arrowSize="1" />

<p v-click="2" class="absolute transform rotate-8" style="left: 610px;top: 210px;">Me</p>
<arrow v-click="2" x1="600" y1="250" x2="750" y2="270" color="#FFF" width="2" arrowSize="1" />

<p v-click="3" class="absolute transform" style="left: 730px;top: 440px;">Somebody's head</p>
<arrow v-click="3" x1="800" y1="450" x2="840" y2="410" color="#FFF" width="2" arrowSize="1" />

<!-- <div class="flex items-center">
  <div>
    <a href="https://my.prairie.cards/u/umihico" target="_blank" class="text-white">https://my.prairie.cards/u/umihico</a>
    <div>
    X, GitHub, etc.
    </div>
  </div>
  <img src="/assets/qr.png" alt="Umihiko Iwasa" class="w-24 h-24 ml-2">
</div> -->

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
皆さんからはうみさん、うみちゃん、海外の方からは「うみ」と短く呼んでもらっています。


写真はいつもこの、私と、誰かの頭のツーショットの写真を使っています。

スタジオプレーリーというところで働いています。プレーリーカードを作っている会社です。

フルスタックWEBエンジニア、バックエンドマネージャーとして働いています。

好きなものは色々ありますが、AWSが好きです。

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

# What is Prairie Card?

<div class="flex w-full mt-5">
  <img src="/assets/iphone-profile.png" class="h-100 object-cover mt-5">
  <img src="/assets/iphone-bizcard.png" class="h-100 object-cover mx-6 mt-5">
  <img src="/assets/demo.gif" class="h-60 object-cover mt-40 ms-10">
</div>
<div v-click=1 class="fixed left-130 top-23 text-xl">
<h2 class="mb-2">Digital Business Card</h2>
<li><span>No App & Camera Required</span></li>
<li><span>Eco-friendly</span></li>
<li><span>Customizable contents and card design</span></li>
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

また、はじめましてのタイミングから、会話が盛り上がる共通点を探すまでに時間がかかるのが普通だと思います。ですが、プレーリーカードはテキストやコンテンツで自己紹介ができているので、相手が気になるものがあれば拾ってくれます。そうすることで、今までは本当は共通点があるのに、うまく見つけられないまま終わってしまった、そういったことが減らせるようになります。
-->

---
layout: intro
transition: slide-left
---

<div class="flex justify-center align-items-center">
<h1 class="pt-3">Swag for speakers 🎉 　</h1>
<img v-mark.orange=1 src="/assets/logo.png" class="w-50 pb-2">
</div>

<div class="grid grid-cols-2 text-center justify-items-center mt-10">
<img src="/assets/swag.png" class="h-80">
<img src="/assets/swag_tweet.png" class="h-80">
<span class="text-xs">https://jawspankration2024.jaws-ug.jp/en/news/jehfb2uqlw/</span>
<span class="text-xs">https://x.com/jawsdays/status/1818978512575062221</span>
</div>

<style>
h1 {
  font-size: 2em !important;
}
.slidev-layout{
  background-color: #499DA2;
}
</style>

<!--
今回スポンサーとして、SWAGのひとつとしてプレーリーカードを、提供させていただきました。
スピーカーの皆様に届いていると思います。

プレーリーカードは自由にデザインしたカードを発行できます。今回はJAWS　pankrationのカッコいいロゴを印字していただきました。裏面はJAWSのアイコンがレトロな格闘ゲームに差し込まれたデザインになっています。

登壇者の方々に使ってもらえたら嬉しいです。
また、リスナーの皆様も登壇者と方といつかお話するきっかけがあれば、見せてくださいと会話のきっかけにしてもらえたら嬉しいです。

JAWS-UGなど人数が多く、カジュアルに出会う機会が多いコミュニティにはピッタリだと思いますので、皆様も是非、検討してもらえたら嬉しいです。月額は無料で、約＄３０くらいになっています。
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

# Quiz: Prairie Card's AWS Architecture

<p class="h-5"></p>

<div class="grid grid-cols-3 gap-4 justify-items-center">
  <div class="text-center text-3xl">
    Amplify?
  </div>
  <div class="text-center text-3xl">
    ECS?
  </div>
  <div class="text-center text-3xl">
    App Runner?
  </div>
  <img src="/assets/amplify.png" class="h-25 w-25 mt-2">
  <img src="/assets/ecs.png" class="h-25 w-25 mt-2">
  <img src="/assets/apprunner.png" class="h-25 w-25 mt-2">
</div>

<p class="h-5"></p>

<div class="text-xl">
  
<div v-click=1>🤔 We are just one year+ old startup</div>
<div v-click=2>🤔 Our human resources is limited</div>
<div v-click=3>🤔 Our traffic is not so high</div>

<p class="h-1"></p>

<div v-click=4>Therefore...?</div>
</div>
<h2 v-click=5>We are using them ALL and we are happy with it! 🤤</h2>

<!--
それでは本題に移りたいと思います。

最初はクイズ形式で、プレーリーカードの状況を伝えるので、どのAWSサービスを使っているか是非考えてみてもらえたらと思います。


・私達はサービスインしてまだ１年ちょっとのスタートアップです。
・私達のエンジニアリソースは非常に限られています。
・私達のトラフィックはそんなに高くないです。

皆様なら、どのようなインフラを選ぶでしょうか。

答えですが、３つとも全て使っています。そして、それで良い選択をしたと思っています。

通常、立ち上がり初期のサービスでは多くのサービスでホスティングしないと思うのですが、これから、どういう訳でそうなっているか時系列順に解説させていただきます。
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

# Service Launching (1st Gen)

- Shopify (= Landing Page & EC) was easy to start.
- To use App Runner, <span v-mark.orange=1>we just need to push the image!</span>

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/1st.png" class="h-90 w-100 object-cover">
</div>

<!--
サービスリリースの頃は、開発スピードとユーザー体験を非常に重視していました。なるべくインフラなどに時間をかけたくなかったです。

そのため、LP＆ECにはShopifyを選択して、ノーコードで立ち上げられました。
またプロフィールページの方は初速に定評のあるRailsが採用されました。ホスティングにはAppRunnerが採用されていて、ほぼ全てマネージドでインフラを動かしています。AppRunnerはイメージをプッシュするだけで更新ができ、かつカスタムドメインなどルーティングの設定も非常に簡単に完了できるので、開発リソースをスピードとユーザー体験に投資したい意図に合っていたと思います。
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

# Card designing with Next.js (2nd Gen)

<ul>
<li>React could handle more complex UI (states, draggable and editable elements)</li>
<li>To use Amplify, <span v-mark.orange=1>we just need to push the code!</span>
  <span v-click=2>
    <ul>
      <li>
        <a href="https://docs.aws.amazon.com/amplify/latest/userguide/pr-previews.html">Web previews for pull requests</a> is AWSome!
      </li>
    </ul>
  </span>
</li>
</ul>

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/2nd.png" class="h-80 w-70 object-cover">
  <video muted class="h-80" loop autoplay>
    <source src="/assets/maker.mov" type="video/mp4">
  </video>
</div>

<!--
次に、カードデザインをユーザーが自由に作れる機能が開発されました。

この機能ができる前は、代表がユーザーと一緒にデザインをつくったり、データをもらって入稿するということを手動でやっていました。

これは、Next.jsをAmplifyの上で動かしています。

まず、作りたいものの特性上、ドラッグできる要素や、ステート管理など複雑なフロントのUIが要求されるので、Reactが採用されました。

このとき、Railsの上でReactをマウントする選択肢もあったと思います。しかし、ここではAmplifyを選択しています。

このカードデザイン機能自体は、プロフィールページのログイン基盤と連携する必要がなく、Railsと結合する必要がありません。

そして既存の本番のサービスであるRailsへ自分たちでReactをビルドしてマウントする部分を整えるよりも、AmplifyにNext.jsのコードをプッシュして、Amplifyのマネージド任せでデプロイするのがスピードの観点や既存の本番に影響を与えないという観点で最適でした。

かつ、Web previews for pull requestの機能のおかげで、マージ前にプルリク単位でURLが吐き出されて、デザイナーやプロダクトオーナーが実機で確認できるようになっています。非常に重宝している機能です。
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

# SSH by ECS & Session Manager (3rd Gen)

- AppRunner does not support SSH 😢
- I added Terraform based script, to create temporary ECS on demand
- Port forwarding to RDS is also possible
- IAM based authentication and keeping RDS & ECS on private network is AWSome!

<div class="flex w-full justify-center">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/3rd.png" class="h-75 w-75 object-cover">
</div>

<!--
最後のECSですが、これはAppRunnerの辛いポイントを補うために採用しました。

AppRunnerはSSHをサポートしてないので、Railsの本番コンソールに入ったり、本番DBにつなぐことができません。

そこで、AppRunnerのイメージを借りて、ECSを一時的に立ち上げるTerraformスクリプトを書いて運用しています。必要なときだけ立ち上げて、終わったらリソースを削除しています。

Webのホスティングをしていないので、オートスケールの調整やロードバランサーなどルーティングまで作り込む必要がありません。かなり簡単に書けています。

セッションマネージャーはポートフォワーディングもサポートしているので、本番RDSへの接続もできました。

個人的に好きなのはIAMベースの認証はRDSに追加のセキュリティをもたらしてくれます。また、セッションマネージャーのおかげでRDSとECSをプライベートネットワークに置いたまま接続できるので、セキュアな点も安心です。

以上が、AppRunnerに始まり、Amplify、ECSを採用した経緯になります。

続いて、他の機能要望に対しても、AWSを少し活用するだけで簡単に実現できたプレーリーカードのインフラを紹介させていただきます。
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

# Protection by WAF

- Just select AppRunner as Web ACL's origin. That's it!

<div class="flex w-full justify-center">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/waf.png" class="h-100 w-120 object-cover">
</div>

<!--
まずはWAFです。

悪意のある攻撃に備えて、WAFを設定しようということになりました。これはWAFを立ち上げてから、ワンボタンでAppRunnerにかませることができるので、時間をかけずすぐに備えることができました。

レートリミットを設けたり、怪しいアクセスにはreCAPTCHAで対応したりということが簡単に設定できるようになります。

また、レートリミットなども実行する前に影響範囲を先に調べるカウントモードなどもあり、意図しない影響を抑えることもでき非常に使いやすいです。
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

# Logging by CloudWatch

- CloudWatch is enabled by default with AppRunner
- We just modified Rails log format by adding a gem (lograge)

<div class="flex w-full justify-center">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/cloudwatch.png" class="h-90 w-100 object-cover">
</div>

<!--
次にログ基盤です。

ログ解析やCS対応でログを調査したいということでログの基盤が必要になってきました。

大きくなってくるとFluentやDatadogなど外部サービスに連携させるということも選択肢かと思いますが、ここも最低限に作っています。

AppRunnerを使った時点でCloudwatchに連携されてログが吐き出されているので、これを使えないか調べたところLog Insightがとても使いやすかったです。クエリで検索ができるし、そのクエリをAI生成する機能もあり、要望を伝えると大体１発で検索できます。

Rails側で検索しやすいようにログフォーマットを整えるため、良いgemを見繕って追加するだけで実現できました。
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

# Connecting to BigQuery

- We execute S3 snapshot exportation every day by GitHub Actions

<div class="flex w-full justify-center">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/snapshot.png" class="h-100 w-140 object-cover">
</div>

<!--
次にBigqueryです。

RDSのスナップショットをS3出力する機能がAWS側にあり、スケジュールされたGithub Actionsで毎日バッチで実行しています。

Bigquery側でS3を参照できるData Transfer Serviceがあるので、AWSとGCPのそれぞれ少しずつの調整で実現することができました。

ただ、これは費用観点やリアルタイムな対応がしにくい点があるので、今後必要な時がきたら改善されていくと思います。
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

# Replacing SendGrid's Inbound Parse with SES

- SES->SNS->Lambda was faster a few seconds than Inbound Parse

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/ses.png" class="h-100 w-120 object-cover">
  <img src="/assets/mail_step1.png" class="h-100 object-cover">
  <img src="/assets/mail_step2.png" class="h-100 object-cover">
</div>

<!--
最後紹介する機能は、SESとAWS Lambdaです。

プレーリーカードにはカードを読み取ったユーザーが、プロフィールページを後日また見返せるように、いくつか保存できる方法を提供しています。

１つがメールによる保存です。これはダイアログに従って、メール画面を開き、空メールを送信すると、返信メールとして、プロフィールページの情報が受信できるものになっています。

空メールを送信してもらう形にすることで、ユーザーがわざわざ自分のメールアドレスを入力する手間や打ち間違いのリスク、受診できないリスクを避けています。

この機能のために、受信したメールをJSONに変換して指定したエンドポイントに送ることができる、SendgridのInbound Parseという機能を使っています。

しかし、このメールを送ってから返信までの時間を短くしようとAWSサービスに切り替えてみたところ、SendGridのInboud parseより数秒早いことを発見しました。SESで受信してイベントとしてSNSに通知、SNSからAWS Lambdaを発火させています。改めてAWSが優秀だなぁと思いました。

メール形式によっては追加の実装が必要そうで、まだ本番デプロイには至ってないです。
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

# Ending: Don't aim for perfection

<p class="h-1"></p>

<div class="text-xl">

We don't replace AWS services, but add a bit one by one when we need it.

<li v-click=1>"The Perfect Architecture" can be slow start for startups</li>
<li v-click=2>Replacing with better architecture is time-consuming and often risky</li>
<li v-click=3>If there are pros and cons between some AWS services, how about using both?</li>

</div>

<div class="flex w-full justify-center" v-click=4>
  <img src="/assets/agile.png" class="h-70 object-cover">
</div>
<div class="flex w-full justify-center" v-click=4>
  <span class="text-xs">https://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp</span>
</div>

<div v-click=5 class="fixed bottom-10 right-5 text-3xl">Thank you!</div>
<img v-click=5 src="/assets/logo.png" class="fixed bottom-20 -right-40 w-60 pb-2">

<!--
最後です。エンディングは、「完璧を求めない」という言葉で締めたいと思います。

私達はここまで、既存のAWSサービスをリプレイスせず、必要な時に少しつずつ足していくという形で、ここまでやってきました。

もともと、私には最初から完璧なインフラを作って、長くそれを使いたいという考え方がありました。

しかし、それはスロースタートになり、フェーズによっては正しくないという学びを得ました

また、リプレイスはリスクを伴う方法であり、そのリスクを無くすために時間がかかってしまいます。ですが、本番を変えずにあくまで「足す」という形の方が、往々にして短い時間で、かつインフラが専門でない私も心理的安全性も高い状態で取り組むことができました。

最後はECSとAppRunnerが同居した際の学びですが、似たサービス同士でメリデメを比べたときは、いっそのこと両方使ってみたらどうなんだろう、と今後も考えてみようと思えるようになりました。今までは使うサービスが増えすぎることに心理的な抵抗があったのですが、フラットに検討できるようになったと思います。

AppRunnerでWebのホスティングをマネージドでやりつつ、SSHなど手の届かないときにスポットでECSを使って、個人的には開発工数を大きく下げれたと思います。

最後に、私が好きな画像を引用させていただきます。MVPを作るに当たってのイメージ図です。

上の駄目な例は４ステップで完成してますが、完成までの３ステップの間は誰もハッピーになっていません。

下の例は最終には５ステップかかり全体の時間は少し長くなってますが、それでも、今できる範囲で常に価値提供しているので、ユーザーの満足度を可能な範囲で高めています。

そして、このユーザーというのは顧客のみを意味するものではなく、事業部全体に対しても、開発者がどう価値提供するべきかを示していると思っていて、いつもこれを考えています。

あと今度JAWSユーザーグループのオフサイトイベントに行く際は皆さん、プレーリーカード用意してもらえら嬉しいです。よろしくお願いいたします。
-->
