<template>
  <article class="card">
    <div class="panels">
      <div class="panels__container">
        <a class="panel">
          <router-link to="/Ski" style="text-decoration: none">
            <div class="panel__content" style="background-image: url(https://lh3.googleusercontent.com/BUllzoWAzlx1cRZA9bgINFyPE0wIotkMgQD9k6aSIHVZLDAu8rA9V6TfvpAvEcMB9E5hTKkz88T7h6KZzX6IXcS2_TzWqfKpZYC1IBvreIQp-yL5uzmaoSiuAqVyjjHuFNclVx4gcg=w2400)">
              <h3 class="panel__title">SKI</h3>
            </div>
          </router-link>
        </a>

        <a class="panel">
          <router-link to="/Snowboard" style="text-decoration: none">
            <div class="panel__content" style="background-image: url(https://lh3.googleusercontent.com/EK_KtyUNQVVUEr9wswkfZgomVzNWNDDbiiU6H-QDxQ0yQKYbXp7BzEQ9xSD8leYBnCVHhrVuBEbZgMyC-sXrJRUlB4hHuoRMYiuruKbu4t738MiK1nX1JaOiwkhg7YB_tsCi7PBEwg=w2400)">
              <h3 class="panel__title">SNOWBOARD</h3>
            </div>
          </router-link>
        </a>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: "MainCard",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "./../assets/styles/home.css";

</style>
