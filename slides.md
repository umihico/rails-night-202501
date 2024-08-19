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
<span v-mark.circle.orange="7">https://my.prairie.cards/u/umihico</span> (X, GitHub, etc.)


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


---
layout: intro
transition: slide-left
---

<div v-click=1>
<h1>What is Prairie Card?</h1>
</div>

<ul>
<li v-click=2><span v-mark.orange>Digital Business Card</span> with NFC Technology</li>
<li v-click=3><span v-mark.orange>No App</span> Required</li>
<li v-click=4><span v-mark.orange>No Camera</span> Required</li>
<li v-click=5><span v-mark.orange>Designable</span> as you want
<ul>
  <li v-click=6>Cool examples <a href="https://x.com/hashtag/PrairieFriends">https://x.com/hashtag/<span v-mark.orange>PrairieFriends</span></a></li>
</ul>
</li>
</ul>

<div class="h-28"></div>
<img v-click=1 src="/assets/qr.png" class="w-20 fixed bottom-8 left-115">

### Web

<span v-mark.circle.orange=0>https://my.prairie.cards/u/umihico</span> (X, GitHub, etc.)


<img v-click=2 src="/assets/launch_image.webp" class="fixed bottom-40 right-10 w-98">
<img v-click=3 src="/assets/demo.gif" class="fixed bottom-40 right-10 w-100">
<!-- <img src="/assets/prairie_card_description.webp" class="fixed top-10 right-10 w-80"> -->

<video v-click=5 muted class="fixed bottom-40 right-10 w-102" controls loop>
  <source src="/assets/demo.mov" type="video/mp4">
</video>

<!-- 
  background-image: url("/assets/demo.gif");
  background-repeat: no-repeat;
  background-position: right 5% bottom 50%;
  background-size: 40%; -->
<style>
h1 {
  font-size: 2em !important;
}
.slidev-layout{
  background-color: #499DA2;
}
</style>


---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# As one of awesome swags 🎉

<div class="flex">
<div>
<a href="https://jawspankration2024.jaws-ug.jp/en/news/jehfb2uqlw/">https://jawspankration2024.jaws-ug.jp/en/news/jehfb2uqlw/</a>
<img src="/assets/swag.png" class="h-90 mt-2">
</div>
<div>
<a href="https://x.com/jawsdays/status/1818978512575062221">https://x.com/jawsdays/status/1818978512575062221</a>
<img src="/assets/swag_tweet.png" class="h-90 mt-8">
</div>
</div>

---
transition: slide-left
---

<style>

.slidev-layout{
  background-color: #499DA2;
  height: 100vh;
}
</style>

# Which service does host your website?

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

<div v-click=1>🤔 We are just one year+ old startup</div>
<div v-click=2>🤔 Our human resources is limited</div>
<div v-click=3>🤔 Our traffic is not so high</div>

<p class="h-1"></p>

<div v-click=4>Therefore...?</div>
<h2 v-click=5>We are using them ALL and we are happy with it! 🤤</h2>

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

- Shopify (= Landing Page & EC) is easy to set up
- To use App Runner (= user profile pages), <span v-mark.orange=1>only we need is just to push the image!</span>

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/1st.png" class="h-90 w-100 object-cover">
  <img src="/assets/profile.png" class="h-90 object-cover">
  <img src="/assets/bizcard.png" class="h-90 object-cover">
</div>

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
<li>To use Amplify, <span v-mark.orange=1>only we need is just to push the code!</span>
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
- I add Terraform based script to create temporary ECS on demand
- SSH and port forwarding to RDS with Session Manager
- IAM based authentication and keeping RDS & ECS on private network is AWSome!

<div class="flex w-full justify-center">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/3rd.png" class="h-75 w-75 object-cover">
</div>

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

- SES->Lambda was faster a few seconds than Inbound Parse

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/ses.png" class="h-100 w-120 object-cover">
  <img src="/assets/mail_step1.png" class="h-100 object-cover">
  <img src="/assets/mail_step2.png" class="h-100 object-cover">
</div>

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

We don't replace AWS services, but add a bit one by one when we need it.

<li v-click=1>Preparing "the perfect architecture" can be slow start for startups</li>
<li v-click=2>Replacing with better architecture is time-consuming and often risky</li>
<li v-click=3>If there are pros and cons between some AWS services, using both is sometimes good strategy</li>

<div class="flex w-full justify-center" v-click=4>
  <img src="/assets/agile.png" class="h-70 object-cover">
</div>
<div class="flex w-full justify-center" v-click=4>
  <span class="text-xs">https://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp</span>
</div>

<div v-click=5 class="fixed bottom-10 right-10 text-3xl">Thank you!</div>
