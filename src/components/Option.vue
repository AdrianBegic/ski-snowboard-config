<template>
  <div class="panel">
    <div class="separator">
      <h1>HELOOOO</h1>
    </div>
{{ selectedOption }}
    <button class="back" @click="selector"></button>
  </div>
</template>

<script>
export default {
  name: "Option",
  props: {
    msg: String,
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

<style scoped>
h1 {
  font-size: 2em;
  right: 0;
  bottom: 0;
  position: absolute;
  color: #fff;
  z-index: 999;
  margin: 30px;
}

.panel {
  width: 40%;
  height: 60vh;
  border-radius: 40px;
  display: inline-block;
  text-align: center;
  margin-top: 15vh;
  border: none;
  box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
    rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
    rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
  overflow: hidden;
  background-image: url("./images-components/canada-skiing-header.jpg");
  background-size:cover;
  cursor: default;
}

.separator.reverse {
  transform: rotateX(180deg);
}

.separator {
  right: 0;
  bottom: 0;
  position: absolute;
  width: 80%;
  height: 100%;
}

.separator::after {
  right: 0;
  bottom: 0;
  position: absolute;
  content: "";
  width: 100%;
  height: 110%;
  background-color: #000;
  clip-path: polygon(50% 0, 0 100%, 1000% 100%);
  border-radius: 0px 40px 40px 0px;
}
</style>
