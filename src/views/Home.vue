<template>
  <div class="home">
    <TitleText text="./onn.sh" />
    <ContactLinks />
  </div>
</template>

<script>
import ContactLinks from '@/components/ContactLinks.vue';
import TitleText from '@/components/TitleText.vue';

export default {
  name: 'home',
  components: {
    ContactLinks,
    TitleText
  }
};
</script>
<style scoped>
p {
  font-size: 1em;
  color: rgb(197, 200, 206);
  max-width: 700px;
}
</style>
