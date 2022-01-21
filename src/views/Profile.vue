<template>
  <Background />

  <Option />
</template>

<script>
import Background from "@/components/Background.vue";
import Option from "@/components/Option.vue";

export default {
  name: "Home",
  components: {
    Background,
    Option,
  },
};
</script>

<style scoped>
@import "./../assets/styles/card.css";
</style>
