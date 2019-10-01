<template>
  <div class="links">
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.4.2/css/all.css"
      integrity="sha384-/rXc/GQVaYpyDdyxK+ecHPVYJSN9bmVFBvjA/9eOB+pb3F2w2N6fc5qB9Ew5yIns"
      crossorigin="anonymous"
    />
    <a href="https://github.com/onnenon">
      <i class="fab fa-github"></i>
    </a>
    <a href="mailto:stephen.onnen@gmail.com">
      <i class="far fa-envelope"></i>
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
  font-size: 1vw;
  padding: 0.3em;
  justify-content: flex-start;
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
