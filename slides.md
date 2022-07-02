---
# try also 'default' to start simple
theme: default

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
background: 'assets/home.jpg'

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
      <use id="logo-svg" xlink:href="/assets/nonce-light.svg#layer1" class=""></use>
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
layout: intro
---


# HOW MANY PEOPLE SHOULD TELL YOU SOMETHING BEFORE YOU ACCEPT IT AS TRUTH?



---
layout: intro
---


# HOW DO YOU MEASURE TRUST?


---

# Trust Equation

The Trust Equation uses four objective variables to measure trustworthiness.

<v-clicks>

- Credibility
- Reliability
- Intimacy
- Self-Interest

</v-clicks>

<div v-click at="5" class="text-center">

$\huge T = \dfrac{C + R + I}{S}$

</div>

<!-- 
CREDIBILITY
has to do with the words we speak. In a sentence we might say, “I can trust what she says about intellectual property; she’s very credible on the subject.”

RELIABILITY
has to do with actions. We might say, “If he says he’ll deliver the product tomorrow, I trust him, because he’s dependable.”

INTIMACY
refers to the safety or security that we feel when entrusting someone with something. We might say, “I can trust her with that information; she’s never violated my confidentiality before, and she would never embarrass me.”

SELF-ORIENTATION
refers to the person’s focus. In particular, whether the person’s focus is primarily on him or herself, or on the other person. We might say, “I can’t trust him on this deal — I don’t think he cares enough about me, he’s focused on what he gets out of it.” Or more commonly, “I don’t trust him — I think he’s too concerned about how he’s appearing, so he’s not really paying attention.”

 -->
---

# Trust Model For Spreading Gossip

An example of $r$-neighbour bootstrap is
given by $\mathcal{T}$-bootstrap percolation for the trust family
<br>
<br>
<br>
<br>


$$
\mathcal{T}:=\left\{K^{j} \in \mathbb{N}^{m} \mid \sum_{i=1}^{m} k_{i}^{j}=r\right\}
$$ 

<br>
<br>

<p v-click>

In the most generic set up, the requirement for a gossip to spread is given by the existence of at least one trust vector $K^i$ for which the gossip can be passed by $k_j$ people of type $j$, for all types $j$.
<sup>1</sup>
</p>

<Footnotes separator>
  <Footnote :number=1><a href="https://arxiv.org/abs/1905.11204" rel="noreferrer" target="_blank">Rinni Bhansali, Laura P. Schaposnik</a></Footnote>
</Footnotes>

---

# Trust Network

<img class="w-200 mx-auto" src="/assets/trust_network.jpg">

---
layout: fact
---

<div class="container">
  <h1 class="relative text-8xl font-700 text-center z-0 m-auto top-30">
  IT’S ALL ABOUT PEOPLE
  </h1>
  <img v-click class="relative z-1 opacity-100 mx-auto bottom-40 w-90"
  src="/assets/trust.gif">
</div>
<!--
you shouldn't trust anyone!

The Trust Equation covers the most common meanings of trust that you encounter in everyday business interactions. What’s important to remember is that the meanings are almost entirely personal, not institutional.

People rarely give over their trust to institutions; really they trust other people.

While companies are often described as credible and reliable (the first two components of The Trust Equation), it’s really the people within the companies that make those companies what they are. And intimacy and self-orientation are almost entirely about people.
-->

---
layout: fact
---

<div class="container">
  <h1 class="relative text-8xl font-700 text-center z-0 m-auto">
  PEOPLE USE NATURAL LANGUAGES
  </h1>
</div>


---
layout: statement
---

# SHIFT FROM TRUSTING
# PEOPLE TO TRUSTING NETWORK & $\mathcal{MATH}$

---

# All Sciences together

- Mathematics
  - Probability
  - Cryptography
- Computer Science
  - Network
  - DLT
- Sociology
- Economy

<br>
<br>

###### To build a Trust Model we called a Blockchain


---
layout: section
---

# Trust Model Architecture


---

# Requirements
We need these emergent characteristics to build a real secure trust model

  
  - Availability
  - Transparency
  - Verifiability
  - Reliability
  - Immutability
  - Flexibility
  - Privacy
  - Censorship Resistance
  - Tamper-Proof



<img class="relative bottom-85 left-130 w-90 -z-1" src="/assets/trilemma2.gif">

  <!-- - Shared Public Database
  - P2P Network
  - Cryptography -->


---
layout: section
---

# NETWORK LAYER

---
class: "text-center"
---

<img class="w-full mx-auto" src="/assets/networks.gif">

---
layout: section
---

# DATA LAYER

---

# Distributed Ledger Technology 
DLT is a decentralized database managed by multiple participants, across multiple nodes

<br>
<br>

  - Peer 2 Peer communication protocol
  - All files are timestamped


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

This technology provides a **verifiable** and **auditable** history of all information stored

<img class="abs-br bottom-50 right-20 w-50" src="/assets/dlt.png">


---

# Types of DLTs

<br>

  + Network
    - Public
    - Private

<br>

  + Access
    - Permissioned
    - Permissionless

<img class="abs-tr top-30 right-20 w-100" src="/assets/dlt-types.jpg">

---

# Types of DLTs

<br>

  + Network
    - **Public**
    - Private

<br>

  + Access
    - Permissioned
    - **Permissionless**

<img class="abs-tr top-30 right-20 w-100" src="/assets/dlt-types.jpg">


---
preload: false
---

# Data Structure
Back-linked list of blocks of data, which is ordered

<img v-click-hide class="fixed top-20 w-full mx-auto -z-1" src="/assets/test.gif">


<div v-after>

- **Data**
- **Hash**
  <br>
  <h5 class="opacity-90">

  - Unique identifier for a block and is analogous to a fingerprint for a human

  </h5>
  <h5 class="opacity-90">

  - Generated using a cryptographic hash algorithm:
  <br>
  $Hash=function(\text{data}, \text{previous\textunderscore hash})$

  </h5>
  
- **Previous Hash**
- **Metadata**
  <h5 class="opacity-90">

  - information about the data; e.g., block number, timestamp, etc.

  </h5>
</div>


---
layout: section
---

# SECURITY LAYER

---
preload: false
---

# Authentication
Refers to systems that verify users to the resources

<img v-click-hide class="relative w-120 mx-auto bottom-10 -z-1" src="/assets/pass.gif">


<div v-after class="relative bottom-110"> 

  - Digital Identity
  - Records
  - Provenance

</div>

<div v-click at="2" class="relative bottom-80">

We need a highly secure and proven way to manage identity. Hence, user identities are managed
and verified without the risk of exposing valuable information, such as personal data.

</div>

---
preload: false
---

# 1970s: The Early days of Internet

(1969) The ARPANET was a p2p network

<div v-click class="text-center">
<uim-exclamation-triangle class="text-3xl pt-1 text-red-600 animate-pulse" />
<span class="text-2xl"> Security Problem</span>
</div>

<br>
<br>

<div v-click>

  - **Privacy**
    + How do I ensure that my message has not been modified ?
  
  - **Authenticity**
    + How do I ensure that the message comes from a legitimate person ?

</div>

---
preload: false
---

# 1970s: The Early days of Internet
Secure Communication over Insecure Channel

<br>
<ins>Problem 1</ins> : How do I ensure that my message has not been modified?

<br>

<div v-click-hide>

<img v-motion-fade class="w-220 mt-12 -ml-4 -z-1" src="/assets/p11.png">

</div>


<div v-after>

<img class="relative bottom-94 w-220 mx-auto" src="/assets/p12.png">

</div>

---
preload: false
---

# 1970s: The Early days of Internet
Secure Communication over Insecure Channel

<br>
<ins>Problem 2</ins> : How do I ensure that the message comes from a legitimate person?

<br>


<img class="absolute w-220  -ml-4" src="/assets/p2.png">

---
preload: false
---

# 1970s: 1<sup>st</sup> Solution - Symmetric Cryptography
Secure Communication over Insecure Channel

<br>

  - Alice and Bob <span class="font-bold text-orange-600">share the same key</span>

  - One key for **both** <span class="font-bold text-red-600">Encryption </span>and <span class="font-bold text-green-600">Decryption</span> of messages

  
<br>

<div v-click>

⚠️ Key Exchange Challenge

</div>

---
preload: false
---

# 1970s: The Basics of Public Key Cryptography
Secure Communication over Insecure Channel


  - Given a <span class="font-bold text-red-600">Private Key</span>, you can derive a <span class="font-bold text-green-500">Public Key</span>

  - But you can’t do the process in reverse (derive the Private Key from Public Key)

  
<br>

<div v-click>

<img v-motion-fade class="relative w-120 mx-auto" src="/assets/pk1.png">

</div>

<Footnotes separator>
  <Footnote :number=0><a href="https://ee.stanford.edu/~hellman/publications/24.pdf" rel="noreferrer" target="_blank">Diffie, Whitfield; Hellman, Martin E. (1976)</a></Footnote>
</Footnotes>

---
preload: false
---

# 1970s: Asymmetric Cryptography
Secure Communication over Insecure Channel

<br>
<br>

<span class="text-center text-xl">

2 keys, one for <span class="font-bold text-red-600">Encryption</span>, one for <span class="font-bold text-green-500">Decryption</span>

</span>

---
preload: false
---

# 1970s: Asymmetric Cryptography
Secure Communication over Insecure Channel

<div v-click-hide class="absolute">

  ##### **Step 1.** Alice and Bob Create their own private/secret key (privately, on their computer)
  <br>

  ##### **Step 2.** Alice and Bob derive their public key based on their own private/secret key (still privately, on their computer)

<br>

<img class="relative w-200 mx-auto" src="/assets/pk2.png">

</div>

<div v-after class="absolute">

  ##### **Step 3.** They publish their public key on the internet
  
  <br>
  <br>

<br>

<img class="relative w-200 top-1 left-8" src="/assets/pk3.png">

</div>

---
preload: false
---

# 1970s: Asymmetric Cryptography
Secure Communication over Insecure Channel

<div v-click-hide class="absolute">

  ##### **Step 4.** Bob now can use Alice’s Public Key to encrypt its message
  <br>

<br>

<img class="relative w-200 mx-auto top-1 left-8" src="/assets/pk4.png">

</div>

<div v-after class="absolute">

  ##### **Step 4.** Bob now can use Alice’s Public Key to encrypt its message
  
  <br>

<br>

<img class="relative w-200 top-1 left-8" src="/assets/pk5.png">

</div>


---
preload: false
---

# 1970s: Asymmetric Cryptography
Secure Communication over Insecure Channel

<div v-click-hide class="absolute">

  ##### **Step 5.** Alice can now use her Private Key to decrypt Bob’s message
  <br>

<br>

<img class="relative w-200 mx-auto top-1 left-8" src="/assets/pk6.png">

</div>

<div v-after class="absolute">

  ##### **Step 5.** Alice can now use her Private Key to decrypt Bob’s message
  
  <br>

<br>

<img class="relative w-200 top-1 left-8" src="/assets/pk7.png">

</div>

---
preload: false
---

# 1970s: Asymmetric Cryptography
Secure Communication over Insecure Channel

<br>
<ins>Problem 1</ins> : How do I ensure that my message has not been modified? <span class="text-green-500">Solved</span>

<br>

<ins>Problem 2</ins> : How do I ensure that the message comes from a legitimate person?

---
preload: false
---

# 1970s: Digital Signature
(1979) RSA - First implementation of Digital Signature

<a href="https://people.csail.mit.edu/rivest/Rsapaper.pdf" rel="noreferrer" target="_blank"> <img class="w-140 mx-auto" src="/assets/rsa.jpeg"></a>


---
preload: false
---

# 1970s: Digital Signature
Secure Communication over Insecure Channel

<div class="text-center">

  #### Encrypt > Sign > Verify > Decrypt

  <br>

<br>

<img class="relative w-200 mx-auto" src="/assets/pk8.png">

</div>

---
preload: false
---

# 1970s: Digital Signature
Secure Communication over Insecure Channel

<div class="text-base">

- **Authentic:**<br>when Alice verifies the message with Bob’s public key, she know that he signed
- **Unforgeable:**<br>only Bob knows his private key
- **Not Reusable:**<br>the signature is a function of the document. It can’t be transferred to any other document
- **Unalterable:**<br>if there is any alteration to the document, the signature can no longer be verified with Bob’s public key

</div>

<br>

<div v-click>

<br>
<ins>Problem 1</ins> : How do I ensure that my message has not been modified? <span class="text-green-500">Solved</span>

<br>

<ins>Problem 2</ins> : How do I ensure that the message comes from a legitimate person? <span class="text-green-500">Solved</span>

</div>

---
layout: section
---

# CONSENSUS LAYER

---

# Reaching Consensus
A consensus algorithm is a method of synchronizing the data across a distributed system


<div v-click>

  - Ensures that all the nodes agree to the *__truth__*

  - Ensures that power remains distributed and decentralized.

  - Guarantees that a single chain is followed and that it holds the *__truth__*

  - The rules that nodes follow to ensure that data are **validated**

  - Consensus results in unanimous acceptance of *__truth__* among the participating nodes

  - **Reliability** in a P2P network is achieved by a consensus protocol

  - By design, consensus protocols cannot be replicated as replication or imitating them <br>
   is costly and time-consuming

</div>

---

# Example of Consensus Algorithms


<br>
<br>

  - Chain-based Proof of Work
    > By solving Computationally intensive mathematical *'puzzels'*

  - Chain-based Proof of Stake
    > Energy-efficient alternative to PoW <br>
    > By staking digital items of value

<!-- 
  - PBFT<sup>1</sup> and BFT-based Proof of Stake 
  
  - Chain-based DAG<sup>2</sup>

  - Chain-bsed Hybrid Models


<Footnotes separator>
  <Footnote :number=1>Practical Byzantine Fault Tolerance</Footnote>
  <Footnote :number=2>Direct Acyclic Graphs</Footnote>
</Footnotes>
 -->

---
layout: quote
---

<span class="main-color uppercase text-4xl tracking-wide">
Each consensus algorithm has its own application scenario
</span>

<p class="opacity-70">

There is no absolute good or bad.<br>
The choice of which consensus to use depends on the type of network and data.

</p>

---

# Architecture Overview

<img class="relative w-150 mx-auto bottom-10 -z-1" src="/assets/arch_layers2.png">

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
layout: fact
---

# WE ALL NEED SOME COFFEE

<img class="relative w-40 mx-auto"
src="/assets/coffee.gif">

---
layout: section
---

# IMPLEMENTATIONS

---

# Early Attempts at Electronic Cash

<br>
<br>
<br>

  - **(1998) b-money - [Wei Dai](http://www.weidai.com/bmoney.txt)**
    + Requires a specified amount of computational work  (Hashcash algorithm)
    + The work done is verified by the community who update a collective ledger book.
    + The worker is awarded funds for their effort.
    + Exchange of funds is accomplished by collective book keeping and authenticated with cryptographic hashes.
Contracts are enforced through the broadcast and signing of transactions with digital signatures (i.e., public key cryptography).
  - **(1998) Bit Gold - [Nick Szabo](https://nakamotoinstitute.org/bit-gold/)**

---
layout: quote
---

# “the one thing that’s missing is a reliable e-cash, whereby on the internet you can transfer funds from A to B without A knowing B or B knowing A” 

-Milton Friedman 1999

---
preload: false
---

# Bitcoin
***Satoshi Nakamoto*** is the name used by the presumed pseudonymous person or persons who developed **bitcoin**, authored the bitcoin **white paper**, and created and deployed bitcoin's original **reference implementation**<sup>1</sup>

<v-clicks class="text-base columns-2">

  - <span class="font-bold text-emerald-600">Network Layer</span>
    - Peer 2 Peer<br><br><br>
  - <span class="font-bold text-emerald-600">Data Layer</span>
    - Timestamped
    - Data Structure<br>
        🔹 Data : Transactions<br>
        🔹 Hashing Function: SHA256
  <br>
  <br>
  - <span class="font-bold text-emerald-600">Security Layer</span>
    - Digital Signature<br>
      🔹 Public Key: Wallet Address<br>
      🔹 Private Key: PIN Code 
  - <span class="font-bold text-emerald-600">Consensus Layer</span>
    - Proof of Work ( Mining $\pi$ ) <br>
      🔹 one-CPU-one-vote
    - Incentive<br>
      🔹 Block Rewards<br>
      🔹 Transaction Fees

</v-clicks>


<Footnotes separator>
  <Footnote :number=1><a href="https://bitcoin.org/bitcoin.pdf" rel="noreferrer" target="_blank">Nakamoto, Satoshi. (2008)</a></Footnote>
</Footnotes>

  <!-- - August 2008: domain name bitcoin.org registered
  - October 2008: A Peer-to-Peer Electronic Cash System  posted to a cryptography mailing list       
  - January 2009: Software implementation released as open source

  - May 2010: the first known commercial transaction using bitcoin occurred when programmer Laszlo Hanyecz bought two Papa John's pizzas for 10,000 BTC -->

---

# Bitcoin - Data Structure


<img class="w-full mt-20" src="/assets/btc-data.png">


---

# Bitcoin - Data Structure
Forks

<img class="w-185 mx-auto" src="/assets/fork2.gif">


---

# Bitcoin - Digital Signature


<img class="w-full mt-10" src="/assets/btc-dig.png">

---
preload: false
---

# Bitcoin - Transactions

<img v-click-hide class="absolute w-230 mx-auto" src="/assets/btc-t1.png">

<img v-after class="absolute w-230 mx-auto" src="/assets/btc-t2.png">


---
preload: false
---

# Bitcoin - Transactions

<img v-click-hide class="absolute w-230 mx-auto" src="/assets/btc-t3.png">

<img v-after class="absolute w-230 mx-auto" src="/assets/btc-t4.png">

<Footnotes separator>
  <Footnote :number=0>* Transaction formats significantly differ in cryptocurrencies.  Most are based on the above idea</Footnote>
</Footnotes>


---
preload: false
---

# Bitcoin - Transactions

<img class="absolute w-230 mx-auto" src="/assets/btc-t5.png">

<Footnotes separator>
  <Footnote :number=0>* Transaction formats significantly differ in cryptocurrencies.  Most are based on the above idea</Footnote>
</Footnotes>

---
preload: false
---

# Bitcoin - Transactions


1) Create the transaction
2) Sign the transaction
<div v-click>

3) **Broadcast to the network**
</div>

<img v-click-hide at="1" class="absolute w-230 -z-1 bottom-5" src="/assets/btc-c1.png">

<img v-after class="absolute w-230 mx-auto -z-1 bottom-5" src="/assets/btc-c2.png">


---
preload: false
---

# Bitcoin - Transactions


1) Create the transaction
2) Sign the transaction
3) **Broadcast to the network**

<div class="font-bold text-green-600">

All peers verify and propagate

</div>

<img v-click-hide class="absolute w-230 -z-1 bottom-5" src="/assets/btc-c3.png">


<img v-after class="absolute w-230 mx-auto -z-1 bottom-5" src="/assets/btc-c4.png">


---
preload: false
---

# Bitcoin - Transactions


1) Create the transaction
2) Sign the transaction
3) **Broadcast to the network**

<div class="font-bold text-green-600">

All peers verify and propagate
</div>
<!-- <p class="text-sm w-1/2 text-green-400">
Each node can validate that the transaction has come from Alice and that according to their view of the system, Alice has enough BTC to send one to Bob
</p> -->

<img v-click-hide class="absolute w-230 -z-1 bottom-5" src="/assets/btc-c5.png">


<img v-after class="absolute w-230 mx-auto -z-1 bottom-5" src="/assets/btc-c6.png">

---
preload: false
---

# Bitcoin - Transactions


1) Create the transaction
2) Sign the transaction
3) **Broadcast to the network**

<div class="font-bold text-green-600">

All peers verify and propagate
</div>
<p class="text-sm w-1/2 text-green-400">
Each node can validate that the transaction has come from Alice and that according to their view of the system, Alice has enough BTC to send one to Bob
</p>

<img class="absolute w-230 -z-1 bottom-5" src="/assets/btc-c7.png">

---
layout: section
---

# PROGRAMMABLE BLOCKCHAINS

---

# Blockchain 2.0 Architecture

<img class="relative w-150 mx-auto -z-1" src="/assets/arch_layers3.png">


---

# Blockchain 2.0 Architecture


<img class="relative w-120 mx-auto top-30" src="/assets/arch_layers4.png">



---

# Ethereum - The World Computer
Application blockchains and smart contracts were introduced with Ethereum and represent the next step in blockchains<sup>1</sup>

<v-clicks>

- <span class="font-bold text-emerald-600">Application Layer</span>
  - Smart Contracts<br>
  🔹 Token Systems<br>
  🔹 Financial derivatives and Stable-Value Currencies<br>
  🔹 Identity and Reputation Systems<br>
  🔹 Decentralized File Storage<br>
  🔹 Decentralized Autonomous Organizations<br>
  🔹 And much more!

</v-clicks>

<Footnotes separator>
  <Footnote :number=1><a href="https://ethereum.org/669c9e2e2027310b6b3cdce6e1c52962/Ethereum_Whitepaper_-_Buterin_2014.pdf" rel="noreferrer" target="_blank">Buterin, Vitalik. (2014)</a></Footnote>
</Footnotes>

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

<img v-after class="absolute w-200 mx-auto -z-1 bottom-5" src="/assets/sc.png">


---
layout: section
---
# WHAT'S NEXT?
💻 <carbon-wifi /> <carbon-wallet /> <carbon-code />



---

# Ethereum - Smart Contracts
<br>
<br>

  - **Ethereum Virtual Machine**

  - **Smart Contract Languages**
  - **Web 3.0**
  - **Tokens**
  - **NFTs**

---
preload: false
---

# Smart Contract Development
<br>
<br>

  - **Solidity Language**
  
  - **Write and Build a Contract**
  - **Deploy on Testnet**
  <br>
  <br>



---
preload: false
---

# Smart Contract Development
<br>
<br>

  - **Solidity Language**
  
  - **Write and Build a Contract**
  - **Deploy on Testnet**
  <br>
  <br>

<br>
<div class="text-3xl text-center">

  <div class="text-rose-600 animate-pulse">

  <carbon-idea />
  Web3 Project Competition

  </div>
  <br>
  <br>
  <br>
  <br>
  <div v-click class="text-red-700 animate-bounce">

  <carbon-fire />
  NFT HOT DROP!
  <carbon-fire />
  </div>

</div>

---
layout: center
class: text-center
---

# Learn More

[Website](https://nonce.academy) · [GitHub](https://github.com/nonceacademy) · [Discord](https://discord.link/nonceacademy)
