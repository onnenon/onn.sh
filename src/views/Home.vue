<template>
  <div class="home">
    <TitleText text="./onn.sh" />
    <ContactLinks />
    <HellowWorld />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import ContactLinks from "@/components/ContactLinks.vue";
import TitleText from "@/components/TitleText.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    ContactLinks,
    TitleText
  }
};
</script>
