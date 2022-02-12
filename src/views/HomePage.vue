<template>
  <div class="home">
    <TitleText text="./onn.sh" />
    <ContactLinks />
  </div>
</template>

<script setup lang="ts">
import ContactLinks from "@/components/ContactLinks.vue";
import TitleText from "@/components/TitleText.vue";
</script>
<style scoped>
p {
  font-size: 1em;
  color: rgb(197, 200, 206);
  max-width: 700px;
}
</style>
