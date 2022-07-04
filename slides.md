---
# try also 'default' to start simple
# theme: ./slidev-nonce-theme

favicon: '/assets/nonce-light.svg'

# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: false
# persist drawings in exports and build
drawings: 
  enabled: false
  presenterOnly: true

fonts:
  sans: 'Rubik'
  serif: 'Rubik'

colorSchema: 'dark'
record: false

preload: false

layout: cover
background: 'assets/images/intro.jpg'

title: "A Secure Trust Model"
titleTemplate: '%s - Nonce Academy'
---

<div class="flex justify-center items-center">
  <svg
    id="logo"
    v-motion
    :initial="{ x: 10, y:-800, scale: 0.1, rotate: 0 }"
    :enter="final"
    viewBox="0 0 25 35" class="h-xs w-xs flex-no-shrink">
    <a xlink:href="https://nonce.academy" target="_blank">
      <use id="logo-svg" xlink:href="/assets/images/nonce-light.svg#layer1" class=""></use>
    </a>
  </svg>
</div>

<div class="abs-b pb-10 text-6xl text-white text-opacity-50" style="font-weight:600;">
    <span v-motion-fade :enter="{opacity:1 ,transition: {opacity: {delay: 2000, duration: 5000}}}" style="word-spacing: 10px;"> NONCE ACADEMY PRESENTS </span>  
</div>

<div class="abs-tr m-6 flex gap-2"
    v-motion :initial="{opacity: 0}" :enter="{opacity:1 ,transition: {opacity: {delay: 13000, duration: 1000}}}">
  <!-- <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button> -->
  <a href="https://twitter.com/nonceacademy" target="_blank" alt="GitHub"
    class="text-l icon-btn opacity-50 !border-none !hover:text-white p-0">
    <carbon-logo-twitter />
  </a>
  <a href="https://discord.link/nonceacademy" target="_blank" alt="GitHub"
    class="text-l icon-btn opacity-50 !border-none !hover:text-white p-0">
    <carbon-logo-discord />
  </a>
  <a href="https://github.com/nonceacademy" target="_blank" alt="GitHub"
    class="text-l icon-btn opacity-50 !border-none !hover:text-white p-0">
    <carbon-logo-github/>
  </a>
</div>

<script setup lang="ts">
const final = {
  x: 0,
  y: -30,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 4,
    stiffness: 2,
    mass: 3,
    delay:1500
  }
}
</script>
<style>

svg use{
fill: #EDEDED;
opacity: 0.8
}

#logo:hover {
  -webkit-filter: drop-shadow( 3px 3px 2px rgba(0, 0, 0, .7));
  filter: drop-shadow( 3px 3px 2px rgba(0, 0, 0, .7));
}
svg:hover #logo-svg{
    fill: #DA0037;
}

</style>

---

# Welcome

---
layout: image-left
image: ./assets/images/intros/0xanik.jpg
---

<h1 class="slide-title">Intro</h1>

<h6 class="secondary-title">Presented by Ali Nik</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>


---
layout:default
---

# Previously On Nonce Academy
<div class="center-container" style="border:none">
<a href="https://nonce.academy/talks/a-secure-trust-model" target="_blank" style="border:none">

  <div style="width:600px; height:300px; border: 2px solid var(--main-color); box-shadow: -5px 5px 15px 1px #000000;position:relative; ">
  <img src='/assets/images/old/home.jpg'  style="width:100%;height:100%;resize-mode:contain; position: absolute; top:0; left:0; z-index:1 !important" />

  <div style="position: absolute;  left:0;  height: 300px; width: 600px; z-index: 99; display: flex; flex-direction: column-reverse; align-items: center; ;">
    <div style="background-color:rgba(255, 255, 255, 0.15); height: 20%; width: 70%; margin-bottom:7px; border-radius: 7px; padding: 5px;">
      <h4 style="letter-spacing: 1px; font-weight:bold; font-family: 'Lucida Console', monospace; text-align:center; margin-bottom: 3px">A Secure Trust Model</h4>
      <p class="teritary-title" style="margin-top:-5px;">May 12<sup>th</sup>, 2022</p>
  </div>
  </div>
  </div>
</a>
</div>

---

# Architecture Overview

<img class="relative w-150 mx-auto bottom-10-z-1" src="assets/images/old/arch_layers2.png">

---
layout: quote
---

<span class="main-color uppercase text-4xl tracking-wide">
BLOCKCHAIN IS AN ARCHITECTURAL CONCEPT
</span>

<p class="opacity-70">

that enables the
decentralized, secure,
direct, digital transfer of
data and values.

</p>
---

# Blockchain 2.0 Architecture

<img class="relative w-150 mx-auto " src="assets/images/old/arch_layers3.png">


---
layout: intro
---



# Ali's content placeholder

This is where the content goes


---
layout:default
---
# Sneak Peak!


---
layout: image-left
image: ./assets/images/intros/Dr.farahani.jpg
---

<h1 class="slide-title">A New Era</h1>

<h6 class="secondary-title">Presented by Dr. Hadi Farahani</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>


---

# Dr. Farahani's content placeholder

This is where the content goes


---
layout: image-left
image: ./assets/images/intros/Alimansour.jpg
---

<h1 class="slide-title">Let's DeBank!</h1>

<h6 class="secondary-title">Presented by Ali Mansour</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>


---
layout: center
---


<video controls>
  <source src="assets/videos/bank.mp4" type="video/mp4">
</video>

---
layout: default
---

# "Is my bank working for me or am I working for my bank?"

<b>Banks are dangerous</b>
Nobel prize winners Muhammad Yunus and Joseph Stiglitz have warned that central banking in particular has morphed to keep the status quo in check.

<h3>But up until now, there were no alternatives</h3>


---
layout: section
---

# But what if there was a solution?


---
layout: default
---

# A New Hope

The solution? Decentralized finance, better known as <b>DeFi</b>.

<ul>
<li>"DeFi" is an umbrella term.</li>
<li>DeFi strives to fulfill centralized finance, or CeFi</li>
<li>DeFi is very likely to shake things up at a macroeconomic level</li>
</ul>


---
layout: default
---

# Vs. Centralized Institutions

<ul>
<li>Complete control over finances</li>
<li>Security against inflation</li>
<li>Investments with high ROI</li>
<li>Freedom</li>
<li>No extraneous fees</li>
<li>Total anonymity</li>
<li>Instant loans</li>
</ul>


---
layout: default
---

# DeFi Adoption

Even science says institutional banks will have no choice but to adopt DeFi.
-United Wholesale Mortgage announced they will accept Bitcoin for mortgage repayments.


With the rise of regulation comes even more growth.
<ul>
<li>Singapore now has clear licensing regimes for crypto companies</li>
<li>There are now tools that allow businesses to manage their crypto payments in a compliant manner</li>
</ul>

---
layout: default
---

# What's in Store?

Despite already producing real, working applications that have already attracted billions in capital <a href="https://www.defipulse.com/" target="_blank">(Over 40 billion Total Value Locked (TVL) as July 2022)</a> with a market cap of 500 billion USD DeFi is just beginning to grow.

As of July 2020, the capitalization of all Defi Applications was just 5%.


Billions of people still don’t have access yet!
DeFi is permissionless; all that’s needed is electricity, an internet connection and a smartphone!


---
layout:default
---

# The DARQ Future

DARQ is referred to as Distributed Ledger Technologies, which include technologies such as artificial intelligence (AI), blockchain, cryptocurrency, extended reality, and quantum computing.
Massive industry players like Google, IBM, Amazon, Facebook, etc. are already in the game.

DARQ is likely to have a game-changing effect on a global scale. 

The future is bright!

---
layout: image-left
image: ./assets/images/intros/Dr.rouhani.jpg
---

<h1 class="slide-title">Documents in Blockchain Culture</h1>

<h6 class="secondary-title">Presented by Dr. Shahin Rouhani</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>

---
layout:default
---

# White Paper

A whitepaper is a document released by developers that explains the technology and purpose of the project they are working on. It tells prospective investors how the cryptocurrency was conceived and highlights its purpose. A crypto whitepaper contains various forms of data like statistics, diagrams, and formulas. The goal of this data is to convince prospective investors to invest in that cryptocurrency.

A white paper is a <b>marketing document</b> used to persuade potential customers to learn more or use the service or technology. It should contain:
<ul>
<li>A problem</li>
<li>The solution,</li>
<li>How the token works to create the solution,</li>
<li>The team,</li>
<li>The deployment plan</li>
</ul>

<b>Think of it like a proposal</b>

---
layout: image-right
image: ./assets/images/papers/btc_whitepaper.png
---

# White Paper


One of the most famous whitepapers, considered the gold standard for crypto whitepapers, was <b>‘Bitcoin: A Peer-to-Peer Electronic Cash System’</b>, published by Satoshi Nakamoto in 2008.


---
layout: center
---

# White Paper

<ol>
<li>Understand why the project was created</li>
<li>Figure out the project's real-worl utility</li>
<li>How does the project achieve consensus in the network</li>
<li>How the initial coins were distributed</li>
<li>Technical explanation of the project</li>
<li>Project timeline</li>
</ol>

---
layout: section
---

# Differences Between a White Paper, Yellow Paper, and Beige Paper

The white paper is mandatory. The other two are optional.

---
layout: default
---

# Yellow Paper

A yellow paper is a more technical version of the white paper.
It presents the scientific details of the technology in a very concise way.
If you think of a white paper as a proposal, the yellow paper can be a part two where all the specific details are.

---
layout: default
---

# Beige Paper

A beige paper is a rewrite of a yellow paper for readability. It re-formats the yellow paper into a more organized format and is usually easier to understand. The information on the beige paper is not as difficult to grasp as a yellow paper.

<img src="/assets/images/misc/paper_difficulty.png" />

---
layout: default
---
# Is there a company with all three papers?

Ethereum is an example with all 3 papers. Here's a link to them:<br>
<div style="width: 100%; display: flex; justify-content: space-between; margin-top:30px; margin-bottom: 25px; align-content: center; align-items: center; flex-direction: row;">
<LinkHolder 
  title="Ethereum White Paper" 
  link="https://ethereum.org/en/whitepaper/" 
  style="width:48%;"
  year=2014
  paperName="A Next-Generation Smart Contract and Decentralized Application Platform"
  author="Vitalik Buterin"
/>
<LinkHolder 
  title="Ethereum Yellow Paper" 
  link="https://ethereum.github.io/yellowpaper/paper.pdf" 
  style="width:48%;height: 135px"
  year="2022"
  paperName="Ethereum: A Secure Decentralized Generalised Transaction Ledger"
  author="Gavin Wood"
/>
</div>
<LinkHolder 
  title="Ethereum Beige Paper" 
  link="https://github.com/chronaeon/beigepaper/blob/master/beigepaper.pdf/" 
  style="width:45%;margin: 0 auto;"
  year=2019
  paperName="Beigepaper: An Ethereum Technical Specification"
  author="Micah Dameron"
/>

---
layout: default
---

# What is the Difference Between a White Paper and a Scientific Paper

The term "white paper" comes to us from a 100-year-old practice of government reporting in the UK. 

government agencies provided data to Parliament to help them make decisions, they would offer a short, focused reports on a single topic with white covers. 

This document with information to solve a problem, is now known in many industries as a "white paper." 

Today, white papers are produced for sales purposes by for-profit companies, making them a marketing tool that can often be confused with a neutral scientific paper.


---
layout: image-right
image: ./assets/images/papers/scientific_paper.png
---

# Scientific Paper


A scientific paper is a document reporting the progress of a scientific activity. It shoudl not be biased, and should be based on sound mathematical and/or experimental data and is peer reviewed.

Although recently, peer review for white papers may be necessary.

---
layout: default
---

# Peer Review in Blockchain


On July 18<sup>th</sup> 2018, <em>Wired</em> published a story called <a href="https://www.wired.com/story/why-you-cant-trust-most-cryptocurrency-white-papers/" target="_blank">Why You Can't Trust More Cryptocurrency White Papers</a>.

It describes the worl of blockchain white papers, where many of them are not up to the general standards for published white papers.

The peer review process is suggested for white papers.

---
layout: default
---

# Peer Review in Blockchain

Peer review is a process that gives quality assurance to the process of creating a blockchain

Peer review is a process by which a white paper is sent to a number of experts in the field to assess, and comments are fed back to the author.

Finally, the white paper is published in a blog/open source journal/reference stie where the reader is assured that what is claimed has at least been checked by experts.

---
layout: default
---

# Peer Review

It must be said that non-peer reviewed papers also exist, as some scientists have felt that the peer review process is clumsy and biased.

For examples, please refer to: <a href="https://arxiv.org/archive/math" target="_blank">https://arxiv.org/archive/math</a>


---
layout: default
---

# Green Paper

Green papers are consultation documents produced by the government. The aim of this document is <b>to allow people both inside and outside Parliament to give the department feedback on its policy or legislative propostals</b>.

In blockchain terminology, a green paper is a white paper for an environmentally friendly (green) crypto.



---
layout: full
---
<div class="break-cover">
  <Countdown countdownTime=20 title="Coffee Time!" />
</div>



---
layout: image-left
image: ./assets/images/intros/Amirkhalaj.jpg
---

<h1 class="slide-title">Web2+1</h1>

<h6 class="secondary-title">Presented by Amir Khalaj</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>

---

# Amir Khalaj's content placeholder

This is where the content goes


---
layout: image-left
image: ./assets/images/intros/mort.jpg
---

<h1 class="slide-title">NFTs</h1>

<h6 class="secondary-title">Presented by Morteza Taher</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>

---


# Morteza Taher's content placeholder

This is where the content goes


---
layout: image-left
image: ./assets/images/intros/sepideh.jpg
---

<h1 class="slide-title">Lands</h1>

<h6 class="secondary-title">Presented by Sepideh Cyrus</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>

---

# Sepideh Cyrus's content placeholder

This is where the content goes


---
layout: full
---

<div class="break-cover">
  <CountdownCircular countdownTime=60 title="Lunch Time!" />
</div>

---
layout: image-left
image: ./assets/images/intros/qollak.jpg
---

<h1 class="slide-title">Qollak</h1>

<h6 class="secondary-title">Presented by Ali Nik (ft. Sheedeh Sharif)</h6>


<ul class="content-overview">
  <li>Thing 1
    <ul clas>
      <li>Subtopic 1</li>
      <li>Subtopic 2</li>
      <li>Subtopic 3</li>
    </ul>
  </li>
  <li>Thing 2</li>
  <li>Thing 3</li>
</ul>

---

# Qollak content introduction

This is where the content goes


---
layout: full
---
<div class="break-cover">
  <Countdown countdownTime=20 title="Coffee Time!" />
</div>

----
layout: image-left
image: ./assets/images/intros/farzin.jpg
---

<h1 class="slide-title">Panel</h1>

<h6 class="secondary-title">Presented by many people</h6>


---
layout: center
class: text-center
---

# Learn More

[Website](https://nonce.academy) · [GitHub](https://github.com/nonceacademy) · [Discord](https://discord.link/nonceacademy)
