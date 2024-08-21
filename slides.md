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

# Digital Business Card: Prairie Card

<div class="flex w-full justify-center">
  <img src="/assets/demo.gif" class="h-70 object-cover mt-15">
  <img src="/assets/iphone-profile.png" class="h-100 object-cover mx-6">
  <img src="/assets/iphone-bizcard.png" class="h-100 object-cover">
</div>
<div class="fixed bottom-10 left-10">
<li class="text-xl" v-click=1><span v-mark.orange>No App & No Camera</span></li>
<li class="text-xl" v-click=2><span v-mark.orange>Card design is up to you</span></li>
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
- To use App Runner, <span v-mark.orange=1>only we need is just to push the image!</span>

<div class="flex w-full justify-center gap-4">
  <!-- <img src="/assets/diagram.png" class="h-110 w-160 object-cover"> -->
  <img src="/assets/infra/1st.png" class="h-90 w-100 object-cover">
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
- I added Terraform based script, to create temporary ECS on demand
- Port forwarding to RDS is also possible
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

<div v-click=5 class="fixed bottom-10 right-10 text-3xl">Thank you!</div>
