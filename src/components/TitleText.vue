<template>
  <div class="title">
    <PromptText />
    {{ currentText }}
    <div id="cursor">&#9610;</div>
  </div>
</template>

<script setup lang="ts">
import PromptText from "@/components/PromptText.vue";
import { defineProps, ref, onBeforeMount } from "vue";
const props = defineProps({
  text: {
    type: String,
    required: true,
  },
});

const currentText = ref(" ");

onBeforeMount(() => {
  let time = 0;
  setTimeout(() => {
    [props.text].forEach((char) => {
      setTimeout(() => {
        currentText.value += char;
      }, (time += Math.floor(Math.random() * 175) + 30));
    });
  }, 2700);
});
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Open+Sans");
@import url("https://fonts.googleapis.com/css?family=Titillium+Web");
@import url("https://fonts.googleapis.com/css?family=Ubuntu+Mono");

.title {
  display: flex;
  flex-direction: row;
  user-select: none;
  font-family: "Ubuntu Mono", monospace;
  font-size: 6em;
  font-weight: 300;
  letter-spacing: 0.01em;
  color: #f8f8f2;
}
#cursor {
  animation: blink 1.2s step-end infinite;
  font-family: "Ubuntu Mono", monospace;
}
@keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: rgb(168, 171, 177);
  }
}
@media all and (max-width: 800px) {
  .title {
    font-size: 14vw;
  }
}
</style>
