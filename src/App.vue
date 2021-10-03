<template>
  <div id="app">
    <main>
      <router-view />
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
})
</script>

<style>
body,
html {
  display: flex;
  color: #f0f6fc;
  font-size: 1em;
  background-color: #010409;
  font-family: 'Titillium Web', 'Open Sans', sans-serif;
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
