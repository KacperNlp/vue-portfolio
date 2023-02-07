<template>
  <the-header></the-header>
  <h1>Portfolio</h1>
</template>

<script>
import TheHeader from "./components/layout/TheHeader.vue";

export default {
  name: "App",
  components: { TheHeader },
};
</script>

<style>
#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #e9e8e8;
  background: #20262e;
  min-height: 100vh;
}
</style>
