<template>

  <div class="nav" style="display: block">
    <input type="checkbox" id="nav-check" />
    <div class="nav-header" style="float: left">
      <div class="nav-title">SKI SNOWBOARD</div>
    </div>
    <div class="nav-btn">
      <label for="nav-check">
        <span></span>
        <span></span>
        <span></span>
      </label>
    </div>

    <div class="nav-links">
      <router-link to="/">Home</router-link>
      <router-link to="/about">Configurator</router-link>
      <router-link to="/profile">About</router-link>
    </div>
  </div>

        <router-view/>

</template>



<style>

@import "./assets/styles/main.css";



</style>
