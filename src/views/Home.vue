<template>
  <div class="home">
<Background/>
    <div class="card-div">
      <MainCard />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import MainCard from "@/components/MainCard.vue";
import Background from "@/components/Background.vue";
export default {
  name: "Home",
  components: {
    MainCard,
    Background,
  },
};
</script>

<style scoped>
.card-div {
  width: 100%;
  height: 92vh;
}
</style>
