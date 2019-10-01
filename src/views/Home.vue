<template>
  <div class="home">
    <TitleText text="./onn.sh" />
    <ContactLinks />
  </div>
</template>

<script>
// @ is an alias to /src
import ContactLinks from "@/components/ContactLinks.vue";
import TitleText from "@/components/TitleText.vue";

export default {
  name: "home",
  components: {
    ContactLinks,
    TitleText
  }
};
</script>
