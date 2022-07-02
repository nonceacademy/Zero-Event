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
layout: section
---

# Intro

This is where Ali's introduction goes.

---

# Ali's content placeholder

This is where the content goes

---
layout: section
---
# A New Era

This is where Dr. Farahani's introduction goes.

---

# Dr. Farahani's content placeholder

This is where the content goes


---
layout: section
---
# Let's DeBank!

This is where Ali Mansour's introduction goes.

---

# Ali Mansour's content placeholder

This is where the content goes


---
layout: section
---
# DYOR!

This is where Dr. Rouhani's introduction goes.

---

# Dr. Rouhani's content placeholder

This is where the content goes

---
layout: cover
---

Coffee time!

---
layout: section
---
# DYOR!

This is where Dr. Rouhani's introduction goes.

---

# Dr. Rouhani's content placeholder

This is where the content goes

---
layout: section
---
# Web2 + 1

This is where Amir Khalaj's introduction goes.

---

# Amir Khalaj's content placeholder

This is where the content goes


---
layout: section
---
# NFTs

This is where Morteza Taher's introduction goes.

---

# Morteza Taher's content placeholder

This is where the content goes


---
layout: section
---
# Lands

This is where Sepideh Cyrus's introduction goes.

---

# Sepideh Cyrus's content placeholder

This is where the content goes

---
layout: cover
---

Lunch Time!

---
layout: section
---
# Qollak

This is where the Qollak introduction goes

---

# Qollak content introduction

This is where the content goes


---
layout: cover
---

Coffee Time!

---
layout: section
---
# Panel Time

This is where the panel page


---
layout: center
class: text-center
---

# Learn More

[Website](https://nonce.academy) · [GitHub](https://github.com/nonceacademy) · [Discord](https://discord.link/nonceacademy)
