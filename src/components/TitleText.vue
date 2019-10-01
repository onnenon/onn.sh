<template>
  <div class="title">
    <mark class="prompt">$</mark>
    {{currentText}}
    <div id="cursor">&#9610;</div>
  </div>
</template>

<script>
export default {
  name: "TitleText",
  data() {
    return { currentText: "" };
  },
  props: {
    text: String
  },
  created() {
    let time = 0;
    [...this.text].forEach(char => {
      setTimeout(() => {
        console.log(char);
        this.currentText += char;
      }, (time += Math.floor(Math.random() * 175) + 30));
    });
  }
};
</script>

<style>
.title {
  display: flex;
  flex-direction: row;
  user-select: none;
  font-family: "Overpass Mono", monospace;
  font-size: 5vw;
  font-weight: 300;
  letter-spacing: 0.01em;
  color: #f8f8f2;
}
mark.prompt {
  color: #c678dd;
  background: none;
}
#cursor {
  animation: blink 1.2s step-end infinite;
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