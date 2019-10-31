<template>
  <div class="links">
    <a href="https://github.com/onnenon" aria-label="Stephen Onnen's GitHub Profile">
      <font-awesome-icon :icon="['fab', 'github']" />
    </a>
    <a href="mailto:stephen.onnen@gmail.com" aria-label="Email Stephen Onnen">
      <font-awesome-icon icon="envelope" />
    </a>
  </div>
</template>

<script>
export default {
  name: "ContactLinks"
};
</script>

<style scoped>
.links {
  flex-direction: row;
  font-size: 2em;
  padding: 0.3em;
  justify-content: flex-start;
}
a {
  outline: 0;
}
a:link {
  color: rgb(197, 200, 206);
  text-decoration: none;
  padding: 1em;
}
a:hover {
  color: rgb(230, 233, 239);
}
a:visited:hover {
  color: rgb(230, 233, 239);
}
a:visited {
  color: rgb(197, 200, 206);
  text-decoration: none;
}
@media all and (max-width: 800px) {
  .links {
    font-size: 6vw;
  }
}
</style>
