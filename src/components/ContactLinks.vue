<template>
  <div class="links">
    <a
      href="https://github.com/onnenon"
      aria-label="Stephen Onnen's GitHub Profile"
    >
      <font-awesome-icon :icon="['fab', 'github']" />
    </a>
    <a
      href="https://linkedin.com/in/sconnen/"
      aria-label="Stephen Onnen's LinkedIn Profile"
    >
      <font-awesome-icon :icon="['fab', 'linkedin']" />
    </a>
    <a href="mailto:stephen.onnen@gmail.com" aria-label="Email Stephen Onnen">
      <font-awesome-icon icon="envelope" />
    </a>
  </div>
</template>

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
  color: #8b949e;
  text-decoration: none;
  padding: 1em;
}
a:hover {
  color: #f0f6fc;
}
a:visited:hover {
  color: #f0f6fc;
}
a:visited {
  color: #8b949e;
  text-decoration: none;
}
@media all and (max-width: 800px) {
  .links {
    font-size: 6vw;
  }
}
</style>
