<template>
  <section class="section portfolio" id="portfolio">
    <base-headline><h2>portfolio</h2></base-headline>
    <base-slide-portfolio
      v-for="project in projects"
      :key="project.id"
      :headline="project.headline"
      :imgUrl="project.imgUrl"
      :url="project.url"
      :techStack="project.stack"
    ></base-slide-portfolio>
  </section>
</template>
<script>
import BaseHeadline from "../base/BaseHeadline.vue";
import BaseSlidePortfolio from "../base/BaseSlidePortfolio.vue";

export default {
  name: "SectionPortfolio",
  components: { BaseHeadline, BaseSlidePortfolio },

  data() {
    return {
      projects: [
        {
          headline: "Limberry",
          url: "https://www.limberry.de/",
          stack: ["HTML", "Twig", "Scss", "JavaScript", "Shopware 6"],
          imgUrl: "./portfolio/limberry.PNG",
          id: 1,
        },
        {
          headline: "Powerbar",
          url: "https://www.powerbar.eu/de_DE",
          stack: ["HTML", "Twig", "Scss", "JavaScript", "Vue", "Shopware 6"],
          imgUrl: "./portfolio/powerbar.PNG",
          id: 2,
        },
        {
          headline: "Intersport",
          url: "https://www.intersport.de/",
          stack: ["HTML", "Smarty", "Less", "JavaScript", "PHP", "Shopware 5"],
          imgUrl: "./portfolio/intersport.PNG",
          id: 3,
        },
        {
          headline: "Krahl & Kroschel",
          url: "https://krahl-kroschel.de/",
          stack: [
            "HTML",
            "Scss",
            "JavaScript",
            "PHP",
            "Wordrpess",
            "WooCommerce",
          ],
          imgUrl: "./portfolio/krahl-and-kroschel.PNG",
          id: 4,
        },
      ],
    };
  },
};
</script>
<style lang="scss"></style>
