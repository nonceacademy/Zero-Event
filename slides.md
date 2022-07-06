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



# What's The Plan?



---
layout: image-left
image: ./assets/images/intros/Dr.farahani.jpg
---

<h1 class="slide-title">A New Era</h1>

<h6 class="secondary-title">Presented by Dr. Hadi Farahani</h6>



---
layout: default
---

# An Opportunity on Every Layer
<img class="relative mx-auto" style="height:80%; float:right" src="assets/images/old/arch_layers3.png">

<li>The research opportunities are endless</li>
<li>Different layers have very different research topics</li>




---
layout: default
---

# Level 0: Distributed Ledger Technologies and the P2P Network

<img  src="assets/images/misc/dlt_archs.png" style="float:right;object-fit:contain; width:45%; margin: 20px;">
<p style="text-align:justify">
Distributed Ledger Technologies (DLTs) are a consensus of replicated, shared and synchronized digital data geographically spread across multiple locations using a peer-to-peer network and unlike centralized databases, there is no central 
administrator. 

<li>At their core, they’re no more than simple data structures</li>
<li> The goal is to not trust each other</li>
<li>We're not limited to using the blockchain</li>
</p>




---

# Level 0: Research Opportunities

<b>Why use anything other than a blockchain?</b>
<div style="font-size:15px; margin-bottom:20px">
<li>Tangle is uniquely scalable, quantum resistant (secure against an attack from a quantum computer) and makes micro transactions feasible through low cost fees.</li>
<li>Reach quick consensus with Hashgraph.</li>
<li>With sidechains, merge blockchains together to increase performance.</li>
</div>
<em><u>Further Reading:</u></em>

<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
<LinkHolder 
  link="https://eprint.iacr.org/2016/555.pdf" 
  style="width:48%;"
  year=2016
  paperName="On the Security and Performance of Proof of Work Blockchains"
  author="A. Gervais et al."
/>
<LinkHolder 
  link="https://www.researchgate.net/publication/328349426_A_Review_of_Distributed_Ledger_Technologies_Confederated_International_Conferences_CoopIS_CTC_and_ODBASE_2018_Valletta_Malta_October_22-26_2018_Proceedings_Part_II" 
  style="width:48%;"
  year=2018
  paperName="A Review of Distributed Ledger Technologies"
  author="N. El Ioini & C. Pahl"
/>
</div>
<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
<LinkHolder 
  link="https://ferdinand-steinbeis-institut.de/wp-content/uploads/2020/11/Distributed-Ledger-Definition-and-Demarcation_Burkhardt-und-Werling.pdf" 
  style="width:48%; height: 110px;"
  year=2020
  paperName="Distributed Ledger: Definition & Demarcation"
  author="D. Burkhardt & M. Werling"
/>
<LinkHolder 
  link="http://scis.scichina.com/en/2021/121101.pdf" 
  style="width:48%;"
  year=2021
  paperName="A Survey of Blockchain Consensus Algorithms: Mechanism, Design and Applications"
  author="X. Fu et al."
/>
</div>

---

# Level 1: Consensus Algorithms

Consensus algorithms are a popular research topic.

Chain-based Proof of Work: By solving computationally intensive mathematical *'puzzels'*
<li>Used in Bitcoin and Ethereum 1.0</li>
<li>Too computationally expensive?</li>
<li>Reusable Proof of Work (RPoW): a solution?</li>


---

# Level 1: Research Opportunities


Proof of Stake (POS): Stake digital items of value

<li>There’s more: Proof of Burn (PoB), Proof of Capacity (PoC), and many many more…</li>

Research to customize to your own needs.


---

# Level 2: Blockchain Data Structure

A blockchain is nothing more than a back-linked linked list.
<br>
Cryptography is what holds everything together
<li>Hashing is key</li>

<img class="relative w-150 mx-auto " src="assets/images/misc/simple_blockchain.png">

---

# Level 2: Blockchain Data Structure

With blockchain technologies, we can count on security and decentralization.
<br>
So much more than “just” cryptocurrencies.
<li>At the most basic level, there are tokens too!</li>


---

# Level 2: Research Opportunities

A new solution every day: DeFi, DAOs, and so much more…


The sky is the limit!

---

# Level 3: Blockchain and Game Theory

Game theory is a study of mathematical models of strategic interaction between rational decision-makers. 
<li>Game theory can be used to analyze the strategies of the consensus nodes as well as the interactions among them. </li>

Game theory has many applications in the field of blockchain-based cryptocurrencies, such as
<ul>
<li>Security</li>
<li>Mining Management</li>
<li>Applications of Game Theory on top of a Blockchain Platform</li>
</ul>

---

# Level 3: Research Opportunities

Challenges in the blockchain platform from a game theory perspective include
<ul>
<li>Existence of Nash Equilibria</li>
<li>Implementation of Game Models</li>
</ul>

<em><u>Further Reading:</u></em>

<div style="width:100%; display: flex; justify-content:space-between; margin: 10px 0; ">
<LinkHolder 
  link="https://arxiv.org/pdf/1902.10865.pdf" 
  style="width:48%;"
  year=2019
  paperName="A Survey on Applications of Game Theory in Blockchain"
  author="Z. Liu et al."
/>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Deep knowledge of the mining process, economics of mining, game theory</Footnote>
</Footnotes>

---

# Level 3: (More) Research Opportunities

More open issues and research directions for applications of game theory in blockchain include
<ul>
<li>Throughput Improvement</li>
<li>Alternative Consensus Mechanisms (ex. Proof of Useful Work or Resources (PoUWR))</li>
<li>Permissioned Ledger Types</li>
</ul>

<em><u>Further Reading:</u></em>

<div style="width:100%; display: flex; justify-content:space-between; margin: 10px 0; ">
<LinkHolder 
  link="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9366733" 
  style="width:48%;"
  year=2021
  paperName="A Systematic Review and Empirical Analysis of Blockchain Simulators"
  author="R. Paulavicius et al."
/>
</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Deep knowledge of the mining process, economics of mining, game theory</Footnote>
</Footnotes>

---

# Level 4: Artificial Intelligence and Blockchain

The decentralized AI enables to process and perform analytics or decision making on trusted, digitally signed, and secure shared data that has been transacted and stored on the blockchain, in a distributed and decentralized fashion, without Trusted Third Parties or intermediaries.

<li>Privacy in AI has become a serious issue recently.</li>
<li>AI to overcome the limitations of the blockchain</li>


---

# Level 4: Artificial Intelligence and Blockchain

Several trends and their applications are shown in the table below:

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

<div style="font-size:14px;margin-bottom:5px;">
Blockchains can offer explainability, privacy, and trust to AI-based applications, whereas AI can enhance scalability and security while resolving the personalization and governance issues for blockchain-based technologies. 
</div>

<ul style="font-size:14px;margin-bottom:5px">
<li>Executing AI models within smart contracts</li>
<li>Predicting gas prices</li>
<li>Using AI to analyze data recorded on a blockchain</li>
</ul>
<em><u style="font-size:16px">Further Reading:</u></em>

<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
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
<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
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

<Footnotes separator>
  <Footnote>Concepts Needed: Statistics, Machine Learning, ability to process and mine information from big data</Footnote>
</Footnotes>

---

# Level 5: Internet of Things and Blockchain

<li>Why though?</li>
<li>Blockchain + IoT = BCIoT</li>


---

# Level 5: Research Opportunities

There are still issues such as data management, scalability and communication costs.

Application fields include

<ul style="font-size:16px">
<li>State-of-the-art eHealth frameworks for patient record keeping and tracking</li>
<li>Application of BCIoT for providing seamless connectivity between clients and industrial applications in smart cities</li>
<li>Blockchain-assisted framework for managing large-scale robotics networks, such as Internet-of-Drones (IoD)</li>
</ul>

<em><u>Further Reading:</u></em>
<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
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

<Footnotes separator>
  <Footnote>Concepts Needed: Basic networking, basic ability to process and analyze data at a relatively large scale.</Footnote>
</Footnotes>

---

# Level 6: Cloud Computing and Blockchain


Cloud computing has a data integrity problem, and blockchain can fix that.

In general, there are three major trust risks in cloud computing platforms:
<ol>
<li>Loss of control</li>
<li>Lack of transparency</li>
<li>Lack of a clear security assurance</li>
</ol>

Blockchain can be upgraded into a secure service.

---

# Level 6: Research Opportunities

Blockchain could be a solution – in the future though.

Some future research directions could include:

<ul>
<li>Decentralized trust relationship construction and maintenance</li>
<li>Customized blockchain operation mechanisms for trust</li>
<li>Risk control</li>
</ul>

<em><u>Further Reading:</u></em>
<div style="display:flex; width: 100%;justify-content:space-between; margin: 10px 0;">
<LinkHolder 
  link="https://journalofcloudcomputing.springeropen.com/track/pdf/10.1186/s13677-021-00247-5.pdf" 
  style="width:48%;"
  year=2021
  paperName="Blockchain-Based Trust Management in Cloud Computing Systems: A Taxonomy, Review and Future Directions"
  author="W. Li et al."
/>

</div>

<Footnotes separator>
  <Footnote>Concepts Needed: Advanced networking, parallelization, process management, etc.</Footnote>
</Footnotes>

---
layout: image-left
image: ./assets/images/intros/Alimansour.jpg
---

<h1 class="slide-title">Let's DeBank!</h1>

<h6 class="secondary-title">Presented by Ali Mansour</h6>


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

Already implemented DeFi platforms: 
<ul>
<li>Decentralized Exchanges (DEXs)</li>
<li>Lending</li>
<li>Staking</li>
<li>Swaping</li>
<li>Liquidity Pools</li>
<li>Farming</li>
</ul>


Billions of people still don’t have access yet!
DeFi is permissionless; all that’s needed is electricity, an internet connection and a smartphone!


---
layout:default
---

# The DARQ Future

DARQ includes technologies such as:
<li><b>D</b>: (D)istributed ledger technology</li>
<li><b>A</b>: (A)rtificial intelligence</li>
<li><b>R</b>: Extended (R)eality</li>
<li><b>Q</b>: (Q)uantum Computing</li>


Massive industry players like Google, IBM, Amazon, Facebook, etc. are already in the game.

DARQ is likely to have a game-changing effect on a global scale. 


---
layout: section
---

# The Future is Complicated!


---
layout: image-left
image: ./assets/images/intros/Dr.rouhani.jpg
---

<h1 class="slide-title">Documents in Blockchain Culture</h1>

<h6 class="secondary-title">Presented by Dr. Shahin Rouhani</h6>



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

<img src="/assets/images/misc/paper_difficulty.png" style="margin-left:auto; margin-right:auto" />

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

Government agencies provided data to Parliament to help them make decisions, they would offer a short, focused reports on a single topic with white covers. 

This document with information to solve a problem, is now known in many industries as a "white paper." 

Today, white papers are produced for sales purposes by for-profit companies, making them a marketing tool that can often be confused with a neutral scientific paper.


---
layout: image-right
image: ./assets/images/papers/scientific_paper.png
---

# Scientific Paper


A scientific paper is a document reporting the progress of a scientific activity. It should not be biased, and should be based on sound mathematical and/or experimental data and is peer reviewed.

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




---
layout: section
---

# Web X.Y

---
layout: center
---

<img src="/assets/images/amirkhalaj/1.png" style="object-fit:contain; max-height:500px; margin-right:300px">


---
layout: center
---

<img src="/assets/images/amirkhalaj/2.png" style="object-fit:contain; max-height:500px; ">


---
layout: center
---

<img src="/assets/images/amirkhalaj/3.png" style="object-fit:contain; max-height:500px; margin-left:300px">


---
layout: center
---

<img src="/assets/images/amirkhalaj/4.png" style="object-fit:contain; max-height:500px">

---

# Web 3.0 Features

<ol>
<li>Semantic web</li>
<li>Artificial Intelligence (AI)</li>
<li>3D Graphics</li>
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

<ul>
<li>Developing dApps or Decentralized Applications </li>
<li>Software as a Service (SaaS)</li>
<li>Decentralized finance or DeFi Services</li>
<li>Backend as a Service (BaaS)</li>
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
layout: center
---

<img src="/assets/images/amirkhalaj/5.webp">


---
layout: section
---

# Web 3 is Hard to Develop

---
layout: center
---

<img src="/assets/images/amirkhalaj/6.webp">

---
layout: section
---

# No benefits for mainstream businesses

---
layout: center
---

<img src="/assets/images/amirkhalaj/7.webp">

---
layout: section
---

# Crypto crush will ruin all Web3 perspectives

---
layout: center
---

<img src="/assets/images/amirkhalaj/8.webp">

---
layout: section
---

# The future is here for businesses


---
layout: image-left
image: ./assets/images/intros/mort.jpg
---

<h1 class="slide-title">NFTs</h1>

<h6 class="secondary-title">Presented by Morteza Taher</h6>




---


# Morteza Taher's content placeholder

This is where the content goes


---
layout: image-left
image: ./assets/images/intros/sepideh.jpg
---

<h1 class="slide-title">Lands</h1>

<h6 class="secondary-title">Presented by Sepideh Cyrus</h6>




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


---

# Qollak: Project Definition

<br>

- Deposit Funds

- Break (Withdraw) at a specific time only by the owner   

- Track savings

- Track expenses

- Fun!


<img class="relative bottom-0 left-170 w-50" src="/assets/images/qollak/qollak.gif">

---
layout: section
---

# Implementations
## Blockend

---

# Ethereum - Smart Contracts
Smart contracts are programs that automatically execute transactions if certain conditions are met, without the need of an intermediary

<div v-click-hide>

- Pieces of code running in the Ethereum Virtual Machine

- The environment is highly restricted for security and determinism
- Each contract has code, state and optionally a balance of Ether
- They may be written to represent a contract between parties but they need not
- They are written in a high level language then compiled into bytecode to run in the EVM
</div>

<img v-after class="absolute w-200 mx-auto bottom-0" src="/assets/images/qollak/sc.png">

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
layout: section
---

# Implementations
## Frontend

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
