---
# try also 'default' to start simple
# theme: ./slidev-nonce-theme

favicon: '/assets/images/nonce-light.svg'

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

title: "Zero Event"
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

<div class="my-fact">

## WELCOME TO
# ZERO <sup>1</sup> EVENT: WEB3.0 FOR ALL! <sup>2</sup>
</div>

<Footnotes separator>
  <Footnote :number=1><a href="https://www.cs.utexas.edu/users/EWD/ewd08xx/EWD831.PDF" rel="noreferrer" target="_blank">Dijkstra, Edsger (1982), Why numbering should start at zero</a></Footnote>
  <Footnote :number=2><a href="https://www.cetfund.org/wp-content/uploads/2020/12/CETF-Digital-Equity-Bill-of-Rights-Nov-5-2020.pdf" rel="noreferrer" target="_blank">DIGITAL EQUITY BILL OF RIGHTS</a></Footnote>
</Footnotes>


<style>
.my-fact {
    @apply text-center grid h-full;
  h1 {
    margin-top: -130px;
    @apply text-8xl font-700;
  }
  h1 + p {
    @apply font-700 text-2xl;
  }
}
</style>

---

# Why numbering should start at zero
To denote the subsequence of natural numbers 2, 3, ..., 12 without the pernicious three dots, four conventions are open to us:


$$
a)\ 2 \leq i < 13
$$
$$
b)\ 1 < i \leq 12
$$
$$
c)\ 2 \leq i \leq 12
$$
$$
d)\ 1 < i < 13
$$ 

<br>
<br>

<v-click>

So let us let our ordinals start at zero: an element's ordinal (subscript) equals the number of elements preceding it in the sequence.

</v-click>

---

# DIGITAL EQUITY BILL OF RIGHTS
To insure Digital Equity for all, residents have the right to:

<v-clicks>

- Broadband that is Sufficient and Reliable.
 
- Broadband that is Ubiquitous.
 
- Broadband that is Affordable.
 
- Broadband that Provides Educational Opportunities and Supports Digital Skills Proficiency.
 
- Broadband that Ensures Public Safety and Maintains Peace of Mind.
 
- Broadband that Improves Quality of Life.
 
- Broadband that Supports Economic Prosperity.
 
- Broadband that Attracts Capital Investment.
 
- Broadband that Supports Innovation and Research.
 
- Broadband that Empowers and Enables Participation in the Democracy.

</v-clicks>

---
layout:default
---

# Previously On Nonce Academy
<div class="center-container" style="border:none">
<a href="https://nonce.academy/talks/a-secure-trust-model" target="_blank" style="border:none">

  <div style="width:600px; height:300px; border: 2px solid var(--main-color); box-shadow: -5px 5px 15px 1px #000000;position:relative; ">
  <img src='/assets/images/home.jpg'  style="width:100%;height:100%;resize-mode:contain; position: absolute; top:0; left:0; z-index:1 !important" />

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

<img class="relative w-150 mx-auto bottom-10-z-1" src="assets/images/arch_layers.png">

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

<img class="relative w-150 mx-auto " src="assets/images/arch_layers2.png">


---
layout: intro
---



# What's The Plan?



---
layout: full
---

<img src="assets/images/intros/Dr.farahani.jpg" class="intro-img">

<h1>A New Era</h1>

<h6>Presented by Dr. Hadi Farahani</h6>



---
layout: default
---

# An Opportunity on Every Layer
<img class="relative mx-auto h-4/5 float-right" src="assets/images/arch_layers2.png">

<div class="even-layout">
<li>The research opportunities are endless</li>
<li>Different layers have very different research topics</li>
</div>



---
layout: default
---

# Level 0: Distributed Ledger Technologies and the P2P Network

<img  src="assets/images/misc/dlt_archs.png" class="float-left object-contain w-1/2 m-5">
<p class="text-justify">
Distributed Ledger Technologies (DLTs) are a consensus of replicated, shared and synchronized digital data geographically spread across multiple locations using a peer-to-peer network and unlike centralized databases, there is no central 
administrator. 
</p>
<div class="relative left-11">
<li>At their core, they’re no more than simple data structures</li>
<li> The goal is to not trust each other</li>
<li>We're not limited to using the blockchain</li>
</div>





---

# Level 0: Research Opportunities

<div class="spaced-layout">
<b>Why use anything other than a blockchain?</b>
<div >
<li>Tangle is uniquely scalable, quantum resistant (secure against an attack from a quantum computer) and makes micro transactions feasible through low cost fees.</li>
<li>Reach quick consensus with Hashgraph.</li>
<li>With sidechains, merge blockchains together to increase performance.</li>
</div>
<div>
<div class="further-reading">Further Reading:</div>

<div class="linkholder-hor">
<LinkHolder 
  link="https://eprint.iacr.org/2016/555.pdf" 
  style="width:48%;height:110px"
  year=2016
  paperName="On the Security and Performance of Proof of Work Blockchains"
  author="A. Gervais et al."
/>
<LinkHolder 
  link="http://scis.scichina.com/en/2021/121101.pdf" 
  style="width:48%;"
  year=2021
  paperName="A Survey of Blockchain Consensus Algorithms: Mechanism, Design and Applications"
  author="X. Fu et al."
/>
</div>
</div>
</div>
---

# Level 1: Consensus Algorithms
<br />
<h3>Consensus algorithms are a popular research topic.</h3>

<br /><br />
<b class="slightly-larger-regular-text">Chain-based Proof of Work:</b> <em>By solving computationally intensive mathematical *'puzzels'*.</em>
<div class="indented-list">
<li class="grayed-text">Used in Bitcoin and Ethereum 1.0</li>
<li class="spaced-list-item grayed-text">Too computationally expensive?</li>
<li class="spaced-list-item grayed-text">Reusable Proof of Work (RPoW): a solution?</li>
</div>


---

# Level 1: Research Opportunities

<div class="spaced-layout">
<div/>
<div>

<b class="slightly-larger-regular-text">Proof of Stake (POS):</b> <em>Stake digital items of value</em>
<li style="margin-left: 44px;" class="grayed-text">There’s more: Proof of Burn (PoB), Proof of Capacity (PoC), and many many more…</li>
</div>
<br/>
<h2 class="text-center underline" >Research to customize to your own needs.</h2>
</div>


---

# Level 2: Blockchain Data Structure
<br/>
A blockchain is nothing more than a back-linked linked list.
<br>
Cryptography is what holds everything together

<li class="spaced-list-item grayed-text" style="margin-left:44px">Hashing is key</li>

<img class="w-170 mx-auto" style="position: relative; top:-30px" src="assets/images/misc/simple_blockchain.png">

---

# Level 2: Blockchain Data Structure


<div class="centered-layout">
<h3 class="underline">
With blockchain technologies, we can count on security and decentralization.
</h3>
<ul class="indented-list">
<li class="spaced-list-item grayed-text">So much more than “just” cryptocurrencies.</li>
<li class="spaced-list-item grayed-text">At the most basic level, there are tokens too!</li>
</ul>

</div>

---

# Level 2: Research Opportunities

<div class="spaced-layout">
<div />
<div>
<span class="slightly-larger-regular-text">A new solution every day:</span> <em>DeFi, DAOs, and so much more…</em>
<li style="margin-left:44px" class="grayed-text">The sky is the limit!</li>
</div>

<div>
<div class="further-reading">Further Reading:</div>
<div class="linkholder-hor">
<LinkHolder 
  link="https://www.researchgate.net/publication/328349426_A_Review_of_Distributed_Ledger_Technologies_Confederated_International_Conferences_CoopIS_CTC_and_ODBASE_2018_Valletta_Malta_October_22-26_2018_Proceedings_Part_II" 
  style="width:48%;"
  year=2018
  paperName="A Review of Distributed Ledger Technologies"
  author="N. El Ioini & C. Pahl"
/>
<LinkHolder 
  link="https://ferdinand-steinbeis-institut.de/wp-content/uploads/2020/11/Distributed-Ledger-Definition-and-Demarcation_Burkhardt-und-Werling.pdf" 
  style="width:48%; height: 110px;"
  year=2020
  paperName="Distributed Ledger: Definition & Demarcation"
  author="D. Burkhardt & M. Werling"
/>
</div>
</div>
</div>

---

# Level 3: Blockchain and Game Theory

<div class="even-layout">

<div>
Game theory is a study of mathematical models of strategic interaction between rational decision-makers. 
<li style="margin-left:44px;" class="grayed-text">Game theory can be used to analyze the strategies of the consensus nodes as well as the interactions among them. </li>
</div>

<div>
Game theory has many applications in the field of blockchain-based cryptocurrencies, such as
<ul class="indented-list">
<li>Security</li>
<li>Mining Management</li>
<li>Applications of Game Theory on top of a Blockchain Platform</li>
</ul>
</div>
</div>

---

# Level 3: Research Opportunities

<div class="spaced-layout w-full">
<div />
<div>
<h4>Challenges in the blockchain platform from a game theory perspective include:</h4>
<ul class="indented-list ">
<li>Existence of Nash Equilibria</li>
<li>Implementation of Game Models</li>
</ul>
</div>

<div>
<div class="further-reading">Further Reading:</div>
<div class="linkholder-hor">
<LinkHolder 
  link="https://arxiv.org/pdf/1902.10865.pdf" 
  style="width:48%;"
  year=2019
  paperName="A Survey on Applications of Game Theory in Blockchain"
  author="Z. Liu et al."
/>
</div>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Deep knowledge of the mining process, economics of mining, game theory</Footnote>
</Footnotes>
</div>
---

# Level 3: (More) Research Opportunities
<div class="spaced-layout">
<div>
<h4>More open issues and research directions for applications of game theory in blockchain include:</h4>
<ul class="indented-list">
<li>Throughput Improvement</li>
<li>Alternative Consensus Mechanisms (ex. Proof of Useful Work or Resources (PoUWR))</li>
<li>Permissioned Ledger Types</li>
</ul>
</div>

<div>
<div class="further-reading">Further Reading:</div>

<div class="linkholder-hor">
<LinkHolder 
  link="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9366733" 
  style="width:48%;"
  year=2021
  paperName="A Systematic Review and Empirical Analysis of Blockchain Simulators"
  author="R. Paulavicius et al."
/>
</div>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Deep knowledge of the mining process, economics of mining, game theory</Footnote>
</Footnotes>
</div>
---

# Level 4: Artificial Intelligence and Blockchain

<div class="even-layout h-3/5">
<span class="text-lg">The decentralized AI enables to process and perform analytics or decision making on trusted, digitally signed, and secure shared data that has been transacted and stored on the blockchain, in a distributed and decentralized fashion, without Trusted Third Parties or intermediaries.</span>
<br /><br /><br />
<li style="margin-left:44px">Privacy in AI has become a serious issue recently.</li><br /><br /><br />
<li style="margin-left:44px">AI to overcome the limitations of the blockchain</li>
</div>

---

# Level 4: Artificial Intelligence and Blockchain

<div class="spaced-layout h-11/12">
<h4>Several trends and their applications are shown in the table below:</h4>

<table class="tg">
<thead>
  <tr>
    <th class="tg-0c3p">Trends</th>
    <th class="tg-wotp">Objective(s)</th>
    <th class="tg-wotp">Applications</th>
    <th class="tg-wotp">Blockchain Benefits</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-d9lh">Explainable AI</td>
    <td class="tg-p8mb">Designing trustworthy and interpretable transparent AI algorithms to know why the algorithm is reaching a specific decision</td>
    <td class="tg-d9lh">- Healthcare<br>- Military<br>- Autonomous Vehicles<br></td>
    <td class="tg-0lax">- Trust<br>- Tracing Executions<br>- Reliability<br></td>
  </tr>
  <tr>
    <td class="tg-0lax">Digital Twins</td>
    <td class="tg-baqh">Translating data and intelligence from complex physical systems into applications and simulations in digital world</td>
    <td class="tg-0lax">- Wind Turbines<br>- Aircraft Engines<br>- Offshore Vessels<br></td>
    <td class="tg-0lax">- Trust<br>- Provenance<br>- Reliability<br></td>
  </tr>
  <tr>
    <td class="tg-0lax">Automated Machine Learning</td>
    <td class="tg-baqh">Automating the whole process of machine learning from raw data acquisition to knowledge management in order to reduce manual work and faster application development</td>
    <td class="tg-0lax">- Big Data Analytics<br>- Industry 4.0 Systems<br>- Massive Production of Intelligent Devices<br></td>
    <td class="tg-0lax">- Permanence<br>- Immutability<br></td>
  </tr>
  <tr>
    <td class="tg-d9lh">Hybrid Learning Models</td>
    <td class="tg-p8mb">Combining different machine learning models to reach better informed decisions</td>
    <td class="tg-d9lh">- Real-time<br>- Decision-agnostic<br>- Data source-agnostic<br></td>
    <td class="tg-0lax">- Trust<br>- Provenance<br>- Performance<br></td>
  </tr>
  <tr>
    <td class="tg-0lax">Lean and Augmented Data Learning</td>
    <td class="tg-baqh">Enabling transfer learning among different AI applications to ensure high availability of relevant and accurate data</td>
    <td class="tg-0lax">- Low data availability applications</td>
    <td class="tg-0lax">- Trust<br>- Provenance<br>- Reliability<br></td>
  </tr>
</tbody>
</table>
</div>

<style type="text/css">
.tg  {border-collapse:collapse;border-color:#93a1a1;border-spacing:0;}
.tg td{background-color:#eee;border-color:#93a1a1;border-style:solid;border-width:0px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:0px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-wotp{border-color:inherit;font-family:"Times New Roman", Times, serif !important;font-size:10px;text-align:center;
  vertical-align:top}
.tg .tg-8hko{font-size:x-small;text-align:left;vertical-align:top}
.tg .tg-1l0q{font-size:x-small;text-align:center;vertical-align:top}
.tg .tg-0c3p{border-color:inherit;font-family:"Times New Roman", Times, serif !important;font-size:10px;text-align:left;
  vertical-align:top}
.tg .tg-qkcv{border-color:inherit;font-family:serif !important;font-size:x-small;text-align:left;vertical-align:top}
.tg .tg-lr19{border-color:inherit;font-family:serif !important;font-size:x-small;text-align:center;vertical-align:top}
.tg .tg-r5sc{border-color:inherit;font-family:"Times New Roman", Times, serif !important;font-size:x-small;text-align:left;
  vertical-align:top}
</style>

---

# Level 4: Research Opportunities

<div class="spaced-layout">
<div>
<div class="text-sm">
Blockchains can offer explainability, privacy, and trust to AI-based applications, whereas AI can enhance scalability and security while resolving the personalization and governance issues for blockchain-based technologies. 
</div>

<ul class="indented-list text-xs mb-5">
<li>Executing AI models within smart contracts</li>
<li>Predicting gas prices</li>
<li>Using AI to analyze data recorded on a blockchain</li>
</ul>
</div>

<div>
<div class="further-reading text-sm">Further Reading:</div>

<div class="linkholder-hor">
<LinkHolder 
  link="https://arxiv.org/pdf/1912.06485.pdf" 
  style="width:48%;"
  year=2019
  paperName="Blockchain Intelligence: When Blockchain Meets Artificial Intelligence"
  author="Z. Zheng et al."
/>
<LinkHolder 
  link="https://www.researchgate.net/publication/331241223_Blockchain_Analytics_and_Artificial_Intelligence" 
  style="width:48%;"
  year="2019"
  paperName="Blockchain Analytics and Artificial Intelligence"
  author="D. Dillenberger"
/>
</div>
<div class="linkholder-hor">
<LinkHolder 
  link="https://ieeexplore.ieee.org/ielx7/6287639/8600701/08598784.pdf" 
  style="width:48%;height:110px"
  year=2019
  paperName="Blockchain for AI: Review and Open Research Challenges"
  author="K. Salah et al."
/>
<LinkHolder 
  link="https://link.springer.com/article/10.1007/s10796-022-10279-0" 
  style="width:48%;"
  year="2022"
  paperName="Artificial Intelligence and Blockchain Integration in Business: Trends from a Bibliometric-Content Analysis"
  author="S. Kumar"
/>
</div>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Statistics, Machine Learning, ability to process and mine information from big data</Footnote>
</Footnotes>
</div>
---

# Level 5: Internet of Things and Blockchain

<div class="centered-layout items-center">

<div class="italic">But why would we want to combine these two?</div>

<div class="mt-8 underline font-semibold text-3xl">Blockchain + IoT = BCIoT</div>
</div>


---

# Level 5: Research Opportunities

<div class="spaced-layout h-10/12">
<div>
<h3>There are still issues such as data management, scalability and communication costs. </h3>
<br/>
<div class="ml-5">
Application fields include:

<ul class="indented-list text-sm">
<li class="mt-3">State-of-the-art eHealth frameworks for patient record keeping and tracking</li>
<li class="mt-3">Application of BCIoT for providing seamless connectivity between clients and industrial applications in smart cities</li>
<li class="mt-3">Blockchain-assisted framework for managing large-scale robotics networks, such as Internet-of-Drones (IoD)</li>
</ul>
</div>
</div>

<div>
<div class="further-reading">Further Reading:</div>
<div class="linkholder-hor">
<LinkHolder 
  link="https://arxiv.org/pdf/2001.01841.pdf" 
  style="width:48%;"
  year=2020
  paperName="Towards a Secure Behavior Modeling for IoT Networks Using Blockchain"
  author="J. Ali et al."
/>
<LinkHolder 
  link="https://www.sciencedirect.com/science/article/pii/S2096720921000014" 
  style="width:48%;"
  year="2021"
  paperName="A Survey on the Adoption of Blockchain in IoT: Challenges and Solutions"
  author="A. Uddin"
/>
</div>
</div>
<Footnotes separator>
  <Footnote>Concepts Needed: Basic networking, basic ability to process and analyze data at a relatively large scale.</Footnote>
</Footnotes>
</div>
---

# Level 6: Cloud Computing and Blockchain

<div class="even-layout">
<h3>Cloud computing has a data integrity problem, and blockchain can fix that.</h3>

<div>
In general, there are three major trust risks in cloud computing platforms:
<ol class="indented-list">
<li>Loss of control</li>
<li>Lack of transparency</li>
<li>Lack of a clear security assurance</li>
</ol>
</div>

<h4 class="italic">Blockchain can be upgraded into a secure service.</h4>
</div>
---

# Level 6: Research Opportunities

<div class="spaced-layout h-10/12">
<h3>Blockchain could be a solution – in the future though.</h3>

<div>
Some future research directions could include:

<ul class="indented-list">
<li>Decentralized trust relationship construction and maintenance</li>
<li>Customized blockchain operation mechanisms for trust</li>
<li>Risk control</li>
</ul>
</div>

<div>
<div class="further-reading">Further Reading:</div>
<div class="linkholder-hor">
<LinkHolder 
  link="https://journalofcloudcomputing.springeropen.com/track/pdf/10.1186/s13677-021-00247-5.pdf" 
  style="width:48%;"
  year=2021
  paperName="Blockchain-Based Trust Management in Cloud Computing Systems: A Taxonomy, Review and Future Directions"
  author="W. Li et al."
/>
</div>
</div>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Advanced networking, parallelization, process management, etc.</Footnote>
</Footnotes>

---
layout: full
---

<img src="assets/images/intros/Alimansour.jpg" class="intro-img-left">

<div class="intro-text-right">
<h1>Let's DeBank!</h1>

<h6 c>Presented by Ali Mansour</h6>
</div>


---
layout: center
---


<video controls>
  <source src="assets/videos/bank.mp4" type="video/mp4">
</video>

---
layout: center
---

# "Is my bank working for me or am I working for my bank?"
<br/><br/>
<div class="even-layout">
<b>Banks are dangerous</b><br/>
<em><li class="grayed-text">Nobel prize winners Muhammad Yunus and Joseph Stiglitz have warned that central banking in particular has morphed to keep the status quo in check.</li></em>
<h3 class="text-center mt-12 underline">But up until now, there were no alternatives</h3>
</div>


---
layout: section
---

# But what if there was a solution?
<div>
<span class="slightly-larger-regular-text">"The root problem with conventional currencies is all the trust that's required to make it work. The central bank must be trusted not to debase the currency, but the history of fiat currencies is full breaches of that trust."</span>
<p class="italic w-full grayed-text" style="text-align:end"><em>-Satoshi Nakamoto (2008)</em></p>
</div>

---
layout: default
---

# A New Hope

<div class="centered-layout">
<h3>The solution? Decentralized finance, better known as <b class="underline">DeFi</b>.</h3>

<ul class="indented-list text-lg">
<li class="spaced-list-item grayed-text">"DeFi" is an umbrella term.</li>
<li class="spaced-list-item grayed-text">DeFi strives to fulfill centralized finance, or CeFi</li>
</ul>
</div>

---
layout: default
---

# Vs. Centralized Institutions

<div class="centered-layout h-11/12">
<ul>
<li>Complete control over finances</li>
<li class="spaced-list-item">Security against inflation</li>
<li class="spaced-list-item">Investments with high ROI</li>
<li class="spaced-list-item">Freedom</li>
<li class="spaced-list-item">No extraneous fees</li>
<li class="spaced-list-item">Total anonymity</li>
<li class="spaced-list-item">Instant loans</li>
</ul>
</div>

---
layout: default
---

# What's in Store?

<div class="even-layout h-11/12">

<h3>Already implemented DeFi platforms: </h3>

<ul class="indented-list">
<li>Decentralized Exchanges (DEXs)</li>
<li>Lending</li>
<li>Staking</li>
<li>Swaping</li>
<li>Liquidity Pools</li>
<li>Farming</li>
</ul>

<span class="italic grayed-text">Billions of people still don’t have access yet!</span>


<span class="text-xl"><span class="underline">DeFi is permissionless;</span> all that’s needed is electricity, an internet connection and a smartphone!</span>

</div>

---
layout:default
---

# The DARQ Future

<div class="even-layout">
<h3>DARQ includes technologies such as:</h3>
<ul class="indented-list">
<li><b class="slightly-larger-regular-text">D</b>: <span class="underline">D</span>istributed ledger technology</li>
<li><b class="slightly-larger-regular-text">A</b>: <span class="underline">A</span>rtificial intelligence</li>
<li><b class="slightly-larger-regular-text">R</b>: Extended <span class="underline">R</span>eality</li>
<li><b class="slightly-larger-regular-text">Q</b>: <span class="underline">Q</span>uantum Computing</li>
</ul>

<span class="grayed-text italic">Massive industry players like Google, IBM, Amazon, Facebook, etc. are already in the game.</span>
<br /><br /><br />
<div class="slightly-larger-regular-text underline text-center">DARQ is likely to have a game-changing effect on a global scale.</div> 
</div>

---
layout: section
---

# The Future is Complicated!


---
layout: full
---



<img src="assets/images/intros/Dr.rouhani.jpg" class="intro-img">

<div class="intro-text">
<h1>Documents in Blockchain Culture</h1>

<h6>Presented by Dr. Shahin Rouhani</h6>
</div>


---
layout:default
---

# White Paper

<div class="spaced-layout h-11/12">
<div>
A whitepaper is a document released by developers that explains the technology and purpose of the project they are working on. 

<ul class="indented-list text-sm mt-2">
<li>It tells prospective investors how the cryptocurrency was conceived and highlights its purpose. </li>

<li>A crypto whitepaper contains various forms of data like statistics, diagrams, and formulas. </li>

<li>The goal of this data is to convince prospective investors to invest in that cryptocurrency.</li>
</ul>
</div>

<span class="italic">A white paper is a <b>marketing document</b> used to persuade potential customers to learn more or use the service or technology.</span> 
<br/>

<div>
It should contain:
<ul class="indented-list text-sm mt-2">
<li>A problem</li>
<li>The solution,</li>
<li>How the token works to create the solution,</li>
<li>The team,</li>
<li>The deployment plan</li>
</ul>
</div>

<h3 class="text-center underline">Think of it like a proposal</h3>
</div>

---
layout: image-right
image: ./assets/images/papers/btc_whitepaper.png
---

# White Paper

<div class="centered-layout text-lg">
One of the most famous whitepapers, considered the gold standard for crypto whitepapers, was <p class="slightly-larger-regular-text underline">‘Bitcoin: A Peer-to-Peer Electronic Cash System’</p> published by Satoshi Nakamoto in 2008.
</div>

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
layout: center
---

# Yellow Paper

<div class="text-xl">
A yellow paper is a more technical version of the white paper.
It presents the scientific details of the technology in a very concise way.
If you think of a white paper as a proposal, the yellow paper can be a part two where all the specific details are. </div>

---
layout: default
---

# Beige Paper

<div class="text-xl text-center">A beige paper is a rewrite of a yellow paper for readability. It re-formats the yellow paper into a more organized format and is usually easier to understand. The information on the beige paper is not as difficult to grasp as a yellow paper.</div>

<img src="/assets/images/misc/paper_difficulty.png" style="margin-left:auto; margin-right:auto" />

---
layout: default
---
# Is there a company with all three papers?

<div class="even-layout">

<h4>Ethereum is an example with all 3 papers. Here's a link to them:</h4>
<div class="w-full flex justify-between mt-8 mb-7 content-center items-center flex-row">
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
</div>

---
layout: default
---

# What is the Difference Between a White Paper and a Scientific Paper

<div class="even-layout">
<div>
The term "white paper" comes to us from a 100-year-old practice of government reporting in the UK. 

<li style="margin-left:44px" class="italic mt-3 grayed-text">Government agencies provided data to Parliament to help them make decisions, they would offer a short, focused reports on a single topic with white covers. </li></div>

This document with information to solve a problem, is now known in many industries as a <span class="underline">"white paper"</span>. 

Today, white papers are produced for sales purposes by for-profit companies, making them a marketing tool that can often be confused with a neutral scientific paper.
</div>

---
layout: image-right
image: ./assets/images/papers/scientific_paper.png
---

# Scientific Paper

<div class="even-layout h-2/3 text-xl text-justify">
A scientific paper is a document reporting the progress of a scientific activity. It should not be biased, and should be based on sound mathematical and/or experimental data and is peer reviewed.

<span class="italic grayed-text">Although recently, peer review for white papers may be necessary.</span>
</div>

---
layout: center
---

# Peer Review in Blockchain

<div class="text-xl">
On July 18<sup>th</sup> 2018, <em>Wired</em> published a story called <a href="https://www.wired.com/story/why-you-cant-trust-most-cryptocurrency-white-papers/" target="_blank">Why You Can't Trust More Cryptocurrency White Papers</a>.

<li class="grayed-text italic" style="margin-left:44px">It describes the worl of blockchain white papers, where many of them are not up to the general standards for published white papers.</li>

The peer review process is suggested for white papers.
</div>

---
layout: center
---

# Peer Review in Blockchain

<div class="text-lg">
<li class="spaced-list-item">Peer review is a process that gives quality assurance to the process of creating a blockchain.</li>

<li class="spaced-list-item">Peer review is a process by which a white paper is sent to a number of experts in the field to assess, and comments are fed back to the author.</li>

<li class="spaced-list-item">Finally, the white paper is published in a blog/open source journal/reference site where the reader is assured that what is claimed has at least been checked by experts.</li>
</div>

---
layout: center
---

# Peer Review

<div class="text-2xl">
It must be said that non-peer reviewed papers also exist, as some scientists have felt that the peer review process is clumsy and biased.

<span class="grayed-text italic text-lg">For examples, please refer to: <a href="https://arxiv.org/archive/math" target="_blank">https://arxiv.org/archive/math</a></span>

</div>

---
layout: center
---

# Green Paper

<div class="text-lg">
Green papers are consultation documents produced by the government. The aim of this document is <b>to allow people both inside and outside Parliament to give the department feedback on its policy or legislative propostals</b>.

<div class="text-center text-xl mt-7">In blockchain terminology, a green paper is a white paper for an environmentally friendly (green) crypto.</div>
</div>



---
layout: full
---

<div class="break-cover">
  <Countdown countdownTime=20 title="Coffee Time!" />
</div>

---
layout: full
---


<img src="assets/images/intros/Amirkhalaj.jpg" class="intro-img">

<div class="intro-text">
<h1>Web2+1</h1>

<h6>Presented by Amir Khalaj</h6>
</div>


---
layout: section
---

# Web X.Y

---
layout: center
---

<img src="/assets/images/amirkhalaj/1.png" class="object-contain h-[500px]">


---
layout: center
---

<img src="/assets/images/amirkhalaj/2.png" class="object-contain h-[500px]">


---
layout: center
---

<img src="/assets/images/amirkhalaj/3.png" class="object-contain h-[500px]">


---
layout: center
---

<img src="/assets/images/amirkhalaj/4.png" class="object-contain h-[500px]">

---
layout: center
---

# Web 3.0 Features

<ol class="text-xl indented-list">
<li>Semantic web</li>
<li>Artificial Intelligence (AI)</li>
<li>Three Dimensional</li>
<li>Connectivity</li>
<li>Ubiquity</li>
<li>Decentralized Technology</li>
</ol>

---
layout: fact
---

# You Must Migrate to Web 3.0

---
layout: quote
---


# “It isn’t often you’d hear tech companies described as dinosaurs, but they are indeed now just that and need to evolve or risk being relegated to an era past.”

---
layout: section
---

# Business Opportunities And Ideas for Web 3.0

---
layout: center
---

<img src="/assets/images/amirkhalaj/logos.png" class="float-right object-contain w-1/2 ml-3"/>
<ul class="text-xl">
<li>Developing dApps or Decentralized Applications </li>
<li class="mt-3">Software as a Service (SaaS)</li>
<li class="mt-3">Decentralized finance or DeFi Services</li>
<li class="mt-3">Backend as a Service (BaaS)</li>
</ul>

---
layout: section
---

# Challenges and Issues

---
layout: section
---

# Web 3 is Chaotic

---


<img src="/assets/images/amirkhalaj/5.webp" style="object-fit: contain; width: 80%; position: absolute;left:0;right:0;margin-left:auto;margin-right:auto">


---
layout: section
---

# Web 3 is Hard to Develop

---

<img src="/assets/images/amirkhalaj/6.webp" style="object-fit: contain; height: 90%; position: absolute;left:0;right:0;margin-left:auto;margin-right:auto">

---
layout: section
---

# No benefits for mainstream businesses

---


<img src="/assets/images/amirkhalaj/7.webp" style="object-fit: contain; width: 80%; position: absolute;left:0;right:0;margin-left:auto;margin-right:auto">

---
layout: section
---

# Crypto crush will ruin all Web3 perspectives

---


<img src="/assets/images/amirkhalaj/8.webp" style="object-fit: contain; height: 90%; position: absolute;left:0;right:0;margin-left:auto;margin-right:auto">

---
layout: section
---

# The future is here for businesses


---
layout: full
---




<img src="assets/images/intros/mort.jpg" class="intro-img">

<div class="intro-text">
<h1>NFTs</h1>

<h6>Presented by Morteza Taher</h6>
</div>

---

<img src="/assets/images/mort/intro.jpg" style="object-fit:contain;height:85%;width:70%;margin-left:auto;margin-right:auto;" />

<p style="width:100%;text-align:center">Caravaggio, painted in c. 1598–1599 or 1602</p>


---

<div style="display:flex;justify-content:center;align-items:center;align-content:center;width:100%;height:100%;">
<div style="display:flex;flex-direction:column;min-width:80%;">
<img src="/assets/images/mort/arrow.png" style="height:100px;width:100%;margin-left:auto;" />

<div style="display: flex; flex-direction: row; justify-content: space-between; align-items:center">
<p>Monopoly</p>
<p>Pseudo-Independence</p>
<p>Artist-Centric</p>
</div>

</div>
</div>
---
layout: section
---

# Art Signature Methods

---
layout: full
---

# Mediums:

<ul class="indented-list text-2xl">
<li>Architecture</li>
<li class="mt-5">Sculpture</li>
<li class="mt-5">Painting</li>
<li class="mt-5">Literature</li>
<li class="mt-5">Music</li>
<li class="mt-5">Theater</li>
</ul>

---
layout: section
---

# Mass-Production Art


---
layout: center
---


<video controls>
  <source src="assets/videos/firstnft.mp4" type="video/mp4" >
</video>
---
layout: section
---

# Screen Revolution!


---
layout: full
---

<img src="/assets/images/mort/nft.png" style="object-fit:contain;height:85%;width:80%;margin-left:auto;margin-right:auto;" />

---
layout: section
---

# SMART CONTRACTS AS ARTIST’S AGENT

---
layout: section
---

# Non-Fungible Tokens

---
layout: image
image: './assets/images/mort/nftchart.png'
---

---

<img src="/assets/images/mort/intro.jpg" style="object-fit:contain;height:85%;width:70%;margin-left:auto;margin-right:auto;" />

<p style="width:100%;text-align:center">Louis Finson, painted in c. 1598–1610</p>


---
layout: full
---



<img src="assets/images/intros/sepideh.jpg" class="intro-img">

<div class="intro-text">
<h1>Lands</h1>

<h6>Presented by Sepideh Cyrus</h6>
</div>


---
layout: full
---

<img src="/assets/images/sepideh/0.jpg" style="object-fit:contain;height:85%;width:80%;margin-left:auto;margin-right:auto;" />

---
layout: section
---

# Vision <br />Vs. <br />Imagination

---
layout: full
---

<div style="width:95%;height:80%;position:absolute;top:0;bottom:0;margin-top:auto;margin-bottom:auto;left:0;right:0;margin-left:auto;margin-right:auto;display:flex; flex-direction:row; justify-content: space-between; align-items: center; align-content:center;">
<img src="/assets/images/sepideh/1.jpg" style="object-fit:contain;height:75%;" />
<img src="/assets/images/sepideh/2.jpg" style="object-fit:contain;height:75%;" />
<img src="/assets/images/sepideh/3.png" style="object-fit:contain;height:75%;" />
<img src="/assets/images/sepideh/4.png" style="object-fit:contain;height:75%;" />

</div>

---
layout: section
---


# What is your estimation? <br />How long will it take us to actually live on another planet?


---
layout: section
---

# Maybe <br />Metaverse <br />is <br />Our New Moon


---
layout: center

---

# <div style="text-align:center">Metaverse has Existed for Many Years in Video Games</div>

<img src="/assets/images/sepideh/5.png" style="object-fit:contain;height:85%;width:70%;margin-left:auto;margin-right:auto;" />

---
layout: section
---

# <div style="text-align:left"><b>METAVERSE IS</b><br/> A proposed version of the internet that incorporates three-dimensional virtual environments.</div>

---
layout: image
image: './assets/images/sepideh/6.png'
---


---
layout: default
---
# Metaverse Features

<ol class="indented-list text-xl">
<li>No construction difficulty</li>
<li class="mt-5">No feasible study</li>
<li class="mt-5">No planning committee</li>
<li class="mt-5">No value engineering</li>
<li class="mt-5">No governmental laws</li>
<li class="mt-5">Custom physics</li>
</ol>



---
layout: section
---

# How to Migrate



---
layout: section
---

<div class="w-full text-2xl" style="text-align:start">
<li>3D Modeling and Design</li>
<li class="mt-3">Computer Programming</li>
<li class="mt-3">VR/AR Development</li>
<li class="mt-3">Blockchain / NFT Engineering</li>
<li class="mt-3">Data Skills</li>
<li class="mt-3">UI/UX Design</li>
</div>


---
layout: center
---


<video controls>
  <source src="assets/videos/demo.mp4" type="video/mp4">
</video>



---
layout: full
---
<div style="width:100%;height:100%;background-color: #040204;position:absolute; top:0;bottom:0;right:0;left:0;display:flex;flex-direction:column;justify-content:center;align-items:center;">
<h1 style="width:100%;text-align:center;margin-top:20px;">"The Power of Imagination Makes Us Infinite"</h1>

<img src="/assets/images/sepideh/7.gif" style="object-fit:contain;height:60%;width:70%;margin-left:auto;margin-right:auto;" />
</div>
---
layout: full
---

<div class="break-cover">
  <CountdownCircular countdownTime=60 title="Lunch Time!" />
</div>

---
layout: full
---



<img src="assets/images/intros/qollak.jpg" class="intro-img-left">

<div class="intro-text-right">
<h1>Qollak</h1>

<h6>Presented by 0xanik (ft. Sheedeh Sharif)</h6>
</div>


---

# Qollak: Project Definition

<ul class="indented-list text-2xl">
<li>Deposit Funds</li>

<li class="spaced-list-item">Break (Withdraw) at a specific time only by the owner</li>

<li class="spaced-list-item">Track savings</li>

<li class="spaced-list-item">Track expenses</li>

<li class="spaced-list-item">Fun!</li>
</ul>


<img class="absolute bottom-5 right-5 w-48" src="/assets/images/qollak/qollak.gif">

---

# Ethereum - Smart Contracts
<div class="mb-7 text-xl">
Smart contracts are programs that automatically execute transactions if certain conditions are met, without the need of an intermediary.
</div>
<div v-click-hide class="indented-list">

- Pieces of code running in the Ethereum Virtual Machine

- The environment is highly restricted for security and determinism
- Each contract has code, state and optionally a balance of Ether
- They may be written to represent a contract between parties but they need not
- They are written in a high level language then compiled into bytecode to run in the EVM
</div>

<img v-after class="absolute w-175 right-0 left-0 mx-auto bottom-3 object-contain" src="/assets/images/qollak/sc.png">


---
layout: full
---

<img src="assets/images/qollak/evm1.png" style="position: absolute;height:100%;object-fit:contain;right:0;left:0;margin-right: auto;margin-left:auto;top:0">

---
layout: full
---

<img src="assets/images/qollak/machinespace.png" style="position: absolute;height:100%;object-fit:contain;right:0;left:0;margin-right: auto;margin-left:auto;top:0">

---


# Smart Contract Languages

<v-clicks class="text-base columns-2">

  - <span class="font-bold text-emerald-600">Ethereum</span>
    - LLL
    - Solidity
    - Vyper<br><br>
  - <span class="font-bold text-emerald-600">Cardano</span>
    - Plutus<br><br><br>
  - <span class="font-bold text-emerald-600">EOS</span>
    - C++
    - WASM<br>
  - <span class="font-bold text-emerald-600">Solana</span>
    - Rust
  - <span class="font-bold text-emerald-600">Hyperledger</span>
    - Go
    - Javascript

</v-clicks>

---
layout: section
---

# Implementations
## Blockend


---

# Model and Data Structure

```solidity {all|1|2-6|all}
struct Kid {
    address payable walletAddress;
    string name;
    uint releaseTime;
    uint amount;
    bool broken;
}
```
<v-click>

```solidity {1|2|3|all}
address[] private parents;
mapping(address => mapping(uint => Kid)) public kids;
mapping(address => uint) private kidsCount;
```
</v-click>

---

# Functions


```solidity {1-2,16|3-9}
function addKid(address payable kidWalletAddress, string memory name, uint releaseTime) 
                                                  payable public kidExist(kidWalletAddress){
    kids[msg.sender][getKidsCount()]= Kid(
        kidWalletAddress,
        name,
        releaseTime,
        msg.value,
        false
    );
    if (getKidsCount() == 0){
        parents.push(msg.sender);
    }
    kidsCount[msg.sender] += 1;

    emit KidAdded(msg.sender, kidWalletAddress, msg.value, balanceOf());
}
```

---

# Functions

```solidity {1,5|3|1,5}
function addToKidsQollak(address kidWalletAddress) private {
    (, uint _index) = getKidByAddress(kidWalletAddress);
    kids[msg.sender][_index].amount += msg.value;
    emit KidCharged(msg.sender, kidWalletAddress, msg.value, balanceOf());
}
```
<v-click>

```solidity {1,3|2|all}
function depositForKid(address walletAddress) payable public kidNotExist(walletAddress){
    addToKidsQollak(walletAddress);
}
```
</v-click>

---

# Functions

```solidity {1,11|3-5|6-10|all}
function canBreak() public view returns(bool) {
    (Kid memory _kid, ,int _index) = getMe();
    require(_index != -1 , "You don't have Qollak!");
    require(_kid.broken == false, "Already broken!");
    require(block.timestamp > _kid.releaseTime, "You can't break yet!");
    if (block.timestamp > _kid.releaseTime) {
        return true;
    } else {
        return false;
    }
}
```
<v-click>

```solidity {1,7|3-4|5-6|all}
function breakMyQollak() payable public {
    (Kid memory _kid, address _parent, int _index) = getMe();
    require(msg.sender == _kid.walletAddress, "You must be the kid to break the Qollak!");
    require(_kid.broken == false, "Already broken!");
    _kid.walletAddress.transfer(_kid.amount);
    kids[_parent][uint(_index)].broken = true;
}
```
</v-click>

---
layout: default
---

# Challenges

<ul class="indented-list text-2xl">
<li>High gas fee</li>
<li class="spaced-list-item">Lack of documentation</li>
<li class="spaced-list-item">Security issues (auditability)</li>
<li class="spaced-list-item">Difficult to change</li>
<li class="spaced-list-item">Computation power</li>
<li class="spaced-list-item">Deterministic</li>
</ul>

---
layout: section
---

# Implementations
## Frontend


---
layout: full
---

<img src="assets/images/qollak/layout1.png" style="position: absolute;height:100%;object-fit:contain;right:0;left:0;margin-right: auto;margin-left:auto;top:0">


---
layout: full
---

<img src="assets/images/qollak/layout2.png" style="position: absolute;height:100%;object-fit:contain;right:0;left:0;margin-right: auto;margin-left:auto;top:0">

---
layout: section
---

# How do we implement it? What if the front-end developer doesn't know about Web3?
(No need to worry)


---
layout: center
---

<div style="text-align:center">
<h1>But we obviously need (some) knowledge</h1>

<div class="text-xl my-10 grayed-text">

The barrier to entry appears to be high, even for a simple HTML-based application.


How much knowledge is needed to "talk" to a smart contract on the blockchain?
</div>

<br />
<h2 class="italic">So, where's the happy middle?</h2>

</div>
---
layout: center
---
<div class="text-xl">

# How do we do this?


<div>To use a smart contract in our interface, we don't need any fancy tools or deep knowledge about complex processes whatsoever.</div>
<br />
<br />

First off, we'll need to connect our wallet to our application somehow

<br />

<div class="text-2xl">Then all we'll need is an address and a general "guide" (ABI) for our smart contract</div>

<br />
<br />
</div>
---
layout: section
---

# We're (not) doomed


<img src="assets/images/qollak/thumbsup.gif" class="float-right h-1/2 object-contain ml-7" >

<div class="italic grayed-text">Only thing left is away to connect to the blockchain for us. That sounds scary.</div>
<br />
<br />
<br />
<div class="text-left text-lg">
Thankfully, no need to reinvent the wheel by writing complex code to interact with the blockchain.

<li class="mt-5" style="margin-left:44px"> There are a bunch of libraries out there with code snippets we can use </li>
</div>

---
layout: center
---

# What we'll use!

<div>
<div class="slightly-larger-regular-text ">For Node.js-based frameworks (React, Vue, Svelte, ...): <a href="https://docs.ethers.io/v5/" target="_blank">Ethersjs</a> and <a href="https://web3js.readthedocs.io/en/v1.7.4/" target="_blank">Web3js</a></div>

<img src="assets/images/qollak/web3vethers.png" class="w-3/5 object-contain mx-auto my-7">

<li>The biggest difference boils down to how they interact with the blockchain, but it's really a matter of preference</li>
<br />
<div class="text-center italic text-xl">For Qollak, I'll be using <u>Ethers.js</u></div>
</div>
---

# Connect to wallet:
<div class="spaced-layout">
<div class="text-lg">The way that these frameworks work is that different parts that we need to communicate with the blockchain (e.g. wallet, smart contracts) are all <u>objects</u>.</div>
<li style="margin-left:44px" class="text-sm">Information is given, a connection is made, and the object is created.</li>

So, for instance to connect our wallet (in this case, MetaMask), we'd simply add:

```javascript {1|3-4|all}
import { ethers } from 'ethers';
// ...
let provider = new ethers.providers.Web3Provider(window.ethereum);
provider.send('eth_requestAccounts', []).then(() => {
  let signer = provider.getSigner();
  // We're done!
});
```
<br/>
<div>And we now have a <em>provider</em> and a <em>signer</em> that let us interact with the blockchain, like creating and signing transactions!</div>
</div>
---


# Interface with smart contract

<div class="spaced-layout text-lg">
Following the same logic as before, given a smart contract's ABI and address, we can make a construct that will let us talk to the smart contract deployed on the blockchain:

```javascript {all}
import qollakABI from '/qollak-abi.json';

const qollakAddr = '0x190340Bf48A95fF8Da436D66e3F4873eD96d9c48';

let qollakContract = new ethers.Contract(qollakAddr, qollakABI, signer);
```

<div class="h-12" />

And making a transaction is as simple as a regular function call:

```javascript {all}
// Create a new kid with their own qollak
qollakContract
  .addKid(kid_address, name, break_time))
  .then((res) => {
    console.log('Success!!');
  });

```
</div>

---
layout: fact
---

# And that's it! <br/><sub>(It works!)</sub>

<div class="mt-12">
The rest is up to us!
</div>

---
layout: center
class: text-center
---

# Learn More

[Website](https://nonce.academy) · [GitHub](https://github.com/nonceacademy) · [Discord](https://discord.link/nonceacademy)
