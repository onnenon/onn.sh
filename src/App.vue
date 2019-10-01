<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
body,
html {
  display: flex;
  color: #f8f8f2;
  font-size: 1em;
  background-color: #272c34;
  font-family: "Titillium Web", "Open Sans", sans-serif;
  padding: 0.5em;
}
</style>
