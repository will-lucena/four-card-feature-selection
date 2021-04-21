<template>
  <div class="root">
    <home />
  </div>
</template>

<script>
import Home from "./views/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/styles.scss";
@import "./assets/scss/base.scss";
</style>
