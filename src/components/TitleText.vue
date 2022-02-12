<template>
  <div class="title">
    <PromptText />
    {{ currentText.join("") }}
    <div id="cursor">&#9610;</div>
  </div>
</template>

<script setup lang="ts">
import PromptText from "@/components/PromptText.vue";
import { ref, onMounted } from "vue";

const props = defineProps({
  text: {
    type: String,
    required: true,
  },
});

const currentText = ref(new Array<string>());

onMounted(() => {
  setTimeout(() => {
    let time = 500;
    [...props.text].forEach((char) => {
      setTimeout(() => currentText.value.push(char), time);
      time += Math.floor(Math.random() * 175) + 30;
    });
  }, 2000);
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
  color: #c9d1d9;
}
#cursor {
  animation: blink 1.2s step-end infinite;
  font-family: "Ubuntu Mono", monospace;
  color: #8b949e;
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
