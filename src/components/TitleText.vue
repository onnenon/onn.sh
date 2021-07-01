<template>
  <div class="title">
    <PromptText />
    {{ currentText }}
    <div id="cursor">&#9610;</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import PromptText from 'components/PromptText.vue'

export default defineComponent({
  name: 'TitleText',
  components: {
    PromptText,
  },
  data() {
    return { currentText: ' ' }
  },
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  created() {
    let time = 0
    setTimeout(() => {
      ;[...this.text].forEach((char) => {
        setTimeout(() => {
          this.currentText += char
        }, (time += Math.floor(Math.random() * 175) + 30))
      })
    }, 2700)
  },
})
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans');
@import url('https://fonts.googleapis.com/css?family=Titillium+Web');
@import url('https://fonts.googleapis.com/css?family=Ubuntu+Mono');

.title {
  display: flex;
  flex-direction: row;
  user-select: none;
  font-family: 'Ubuntu Mono', monospace;
  font-size: 6em;
  font-weight: 300;
  letter-spacing: 0.01em;
  color: #f8f8f2;
}
#cursor {
  animation: blink 1.2s step-end infinite;
  font-family: 'Ubuntu Mono', monospace;
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
