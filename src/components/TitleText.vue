<template>
  <div class="title">
    <mark class="prompt">$</mark> ./onn.sh
    <div id="cursor" v-show="true">&#9610;</div>
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
</style>