<template>
  <div class="title">
    <mark class="prompt">$</mark>
    {{text}}
    <div id="cursor">&#9610;</div>
  </div>
</template>

<script>
export default {
  name: "TitleText",
  props: {
    text: String
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
</style>