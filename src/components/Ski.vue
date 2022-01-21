<template>
  <Background />
  <article v-if="visible != true" class="card">
    <h1 class="card-title">SKI</h1>
    <div class="option-container">
      <div id="freestyle" class="optionOne" @click="selector($event)">
        <h1 class="sub-title">FREESTYLE</h1>
        <img id="sub-choice" src="@/assets\images\ski1.png" alt="img" />
      </div>
      <div id="downhill" class="optionTwo" @click="selector($event)">
        <h1 class="sub-title">DOWNHILL</h1>
        <img id="sub-choice" src="@/assets\images\ski2.webp" alt="img" />
      </div>
      <div id="mountain" class="optionThree" @click="selector($event)">
        <h1 class="sub-title">MOUNTAIN</h1>
        <img id="sub-choice" src="@/assets\images\ski1.png" alt="img" />
      </div>
    </div>
    <button class="back" @click="$router.push('/')"></button>
  </article>
  <Option v-if="visible" />
</template>

<script>
import Option from "@/components/Option.vue";

import Background from "@/components/Background.vue";

export default {
  name: "Ski",
  props: {
    msg: String,
  },
  components: {
    Background,
    Option,
  },
  data() {
    return {
      selectedPanel: "",
      visible: false,
    };
  },
  methods: {
    choice: function (event) {
      this.targetId = event.currentTarget.id; // returns 'id'
    },

    selected: function () {
      if (this.targetId === "freestyle") {
        this.selectedPanel = "freestyle";
      } else if (this.targetId === "downhill") {
        this.selectedPanel = "downhill";
      } else {
        this.selectedPanel = "mountain";
      }
      console.log(this.selectedPanel);
    },

    hide() {
      this.visible = true;
    },

    selector() {
      this.choice(event);
      this.hide();
      this.selected();
    },
    
  },
};



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "./../assets/styles/card.css";

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
