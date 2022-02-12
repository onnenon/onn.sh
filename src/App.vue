<template>
  <div id="app">
    <main>
      <HomePage />
    </main>
  </div>
</template>

<script setup lang="ts">
import HomePage from "@/views/HomePage.vue";
</script>

<style>
body,
html {
  display: flex;
  color: #c9d1d9;
  font-size: 1em;
  background-color: #0d1117;
  font-family: "Titillium Web", "Open Sans", sans-serif;
  padding: 0.5em;
}
@media all and (max-width: 800px) {
  .title {
    font-size: 14vw;
  }
  .links {
    font-size: 6vw;
  }
}
</style>
