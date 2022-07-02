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
background: 'assets/images/old/home.jpg'

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
layout: intro
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



# Ali's content placeholder

This is where the content goes

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

# Ali Mansour's content placeholder

This is where the content goes



---
layout: image-left
image: ./assets/images/intros/Dr.rouhani.jpg
---

<h1 class="slide-title">DYOR!</h1>

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

# Dr. Rouhani's content placeholder

This is where the content goes

---
layout: full
---
<div class="break-cover">
  <p> Coffee Time! </p>
  <img src="/assets/images/loading/moving-cube.gif" style="height:50%;resize-mode:contain;width:50%;">
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
  <img src="/assets/images/loading/moving-circle.gif" style="height:80%;resize-mode:contain">
  <p class="absolute-center">Lunch Time</p>
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
  <p> Coffee Time! </p>
  <img src="/assets/images/loading/moving-cube.gif" style="height:50%;resize-mode:contain;width:50%;">
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
