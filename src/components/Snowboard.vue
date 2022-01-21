<template>
  <Background />
  <article v-if="visible != true" class="card">
    <h1 class="card-title">SNOWBOARD</h1>
    <div class="option-container">
      <div class="optionOne" @click="selector">
        <h1 class="sub-title">FREESTYLE</h1>
        <img id="sub-choice" src="@/assets\images\board1.png" alt="img" />
      </div>
      <div class="optionTwo" @click="selector">
        <h1 class="sub-title">ALL MOUNTAIN</h1>
        <img id="sub-choice" src="@/assets\images\board1.png" alt="img" />
      </div>
      <div class="optionThree" @click="selector">
        <h1 class="sub-title">ALPINE</h1>
        <img id="sub-choice" src="@/assets\images\board1.png" alt="img" />
      </div>
    </div>
    <button class="back" @click="$router('Snowboard')"></button>
  </article>
  <Option v-if="visible" />
</template>

<script>
import Option from "@/components/Option.vue";
import Background from "@/components/Background.vue";

export default {
  name: "Snowboard",
  props: {
    msg: String,
  },
  components: {
    Background,
    Option,
  },
  data() {
    return {
      visible: false,
    };
  },
  methods: {
    hide() {
      this.visible = true;
    },

    choice() {
      console.log(999);
    },

    selector() {
      this.hide();
      this.choice();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "./../assets/styles/card.css";
</style>
