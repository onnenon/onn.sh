<template>
  <div id="app">
    <main>
      <router-view />
    </main>
  </div>
</template>

<style>
body,
html {
  display: flex;
  color: #f8f8f2;
  font-size: 1em;
  background-color: #272c34;
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
