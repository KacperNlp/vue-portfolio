<template>
  <section class="tech-stack">
    <base-headline
      ><h2 class="tech-stack-headline">tech. stack</h2></base-headline
    >
    <div class="tech-stack-list">
      <base-tile v-for="tech in techStack" :key="tech" :text="tech"></base-tile>
    </div>
  </section>
</template>
<script>
import BaseHeadline from "../base/BaseHeadline.vue";
import BaseTile from "../base/BaseTile.vue";

export default {
  name: "SectionTechStack",
  components: { BaseHeadline, BaseTile },

  data() {
    return {
      techStack: [
        "HTML",
        "CSS",
        "Sass",
        "Less",
        "JavaScript",
        "TypeScript",
        "React",
        "Vue",
        "Wordpress",
        "Shopware",
        "Twig",
        "PHP",
        "Jest",
        "Smarty",
        "Nuxt",
      ],
    };
  },
};
</script>
<style lang="scss">
.tech-stack {
  &-headline {
    margin-bottom: 40px;
  }

  &-list {
    display: flex;
    flex-wrap: wrap;
    grid-gap: 30px;
  }
}
</style>
