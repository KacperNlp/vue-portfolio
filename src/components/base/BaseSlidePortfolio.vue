<template>
  <div class="base-slide-portfolio">
    <div class="base-slide-portfolio-img">
      <img :src="imgUrl" :alt="headline" />
    </div>
    <div class="base-slide-portfolio-details">
      <h3 class="base-slide-portfolio-details-headline">{{ headline }}</h3>
      <a
        :href="url"
        class="base-slide-portfolio-details-link"
        target="_blank"
        >{{ url }}</a
      >
      <ul class="base-slide-portfolio-details-tech-stack-list">
        <li
          class="base-slide-portfolio-details-tech"
          v-for="tech in techStack"
          :key="tech"
        >
          {{ tech }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "BaseSlidePortfolio",
  props: {
    headline: {
      type: String,
      required: true,
    },
    techStack: {
      type: Array,
      required: true,
    },
    imgUrl: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
};
</script>
<style lang="scss">
.base-slide-portfolio {
  display: flex;
  flex-direction: column;
  grid-gap: 20px;

  @media (min-width: 1024px) {
    flex-direction: row;
  }

  &-img {
    width: 450px;
    height: 280px;

    img {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
