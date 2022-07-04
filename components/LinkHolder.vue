<script setup lang="ts">
import { ref } from "vue";

const props = defineProps({
  link: {
    default: "http://www.scholar.google.com",
  },
  title: {
    default: "",
  },
  paperName: {
    default: "Paper name here!",
  },
  author: {
    default: "Author name here",
  },
  year: {
    default: 2020,
  },
});

const counter = ref(props.link);
</script>

<template>
  <div style="border: 2px solid #aaa; padding: 3px">
    <a :href="link" target="_blank">
      <h6 class="title-text" v-if="title.length > 1">{{ title }}</h6>
      <div class="base-container">
        <div>
          <h4 style="text-align: center">
            {{ paperName }}
            <em
              ><sub>({{ year }})</sub></em
            >
          </h4>
        </div>
        <h5>{{ author }}</h5>
      </div>
    </a>
  </div>
</template>

<style scoped>
.base-container {
  background-color: #070707;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  padding: 10px 5px;
}

.title-text {
  text-align: center;
}
</style>