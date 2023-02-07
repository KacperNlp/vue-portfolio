<template>
  <the-header></the-header>
  <main class="main">
    <div class="main-fixed-image">
      <the-fixed-image></the-fixed-image>
    </div>
    <div class="main-content">
      <section-about-me></section-about-me>
      <section-my-service></section-my-service>
      <section-tech-stack></section-tech-stack>
    </div>
  </main>
</template>

<script>
//layout
import TheFixedImage from "./components/layout/TheFixedImage.vue";
import TheHeader from "./components/layout/TheHeader.vue";

//sections
import SectionAboutMe from "./components/sections/SectionAboutMe.vue";
import SectionMyService from "./components/sections/SectionMyService.vue";
import SectionTechStack from "./components/sections/SectionTechStack.vue";

export default {
  name: "App",
  components: {
    TheFixedImage,
    TheHeader,
    SectionAboutMe,
    SectionMyService,
    SectionTechStack,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Roboto Condensed", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #e9e8e8;
  background: #20262e;
  min-height: 100vh;
}

.main {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  padding: 0 20px;
  grid-gap: 50px;

  &-fixed-image {
    display: none;
  }

  @media (min-width: 1280px) {
    grid-template-columns: repeat(2, 1fr);
    padding-left: 0;

    &-fixed-image {
      display: block;
    }

    &-content {
      padding-right: 40px;
    }
  }

  @media (min-width: 1660px) {
    &-content {
      padding-right: 80px;
    }
  }
}

.section {
  position: relative;
  margin-bottom: 70px;
  padding-bottom: 40px;

  @media (min-width: 1280px) {
    margin-bottom: 110px;
    padding-bottom: 60px;
  }

  &::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 1px;
    background: #545960;
  }
}
</style>
