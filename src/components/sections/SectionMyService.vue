<template>
  <section class="section my-servie" id="my-servie">
    <base-headline
      ><h2 class="my-servie-headline">my service</h2></base-headline
    >
    <div class="my-servie-tiles">
      <base-service
        v-for="service in services"
        :key="service.id"
        :headline="service.headline"
        :description="service.description"
      ></base-service>
    </div>
  </section>
</template>
<script>
import BaseHeadline from "../base/BaseHeadline.vue";
import BaseService from "../base/BaseService.vue";

export default {
  name: "SectionMyService",
  components: { BaseHeadline, BaseService },

  data() {
    return {
      services: [
        {
          headline: "development",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra tincidunt diam, ac commodo orci ullamcorper eu. Nulla imperdiet, mi lobortis",
          id: 1,
        },
        {
          headline: "SEO optimization",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra tincidunt diam, ac commodo orci ullamcorper eu. Nulla imperdiet, mi lobortis",
          id: 2,
        },
        {
          headline: "performance",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra tincidunt diam, ac commodo orci ullamcorper eu. Nulla imperdiet, mi lobortis",
          id: 3,
        },
        {
          headline: "performance",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra tincidunt diam, ac commodo orci ullamcorper eu. Nulla imperdiet, mi lobortis",
          id: 4,
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.my-servie {
  &-headline {
    margin-bottom: 30px;

    @media (min-width: 768px) {
      margin-bottom: 90px;
    }
  }

  &-tiles {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 60px;

    @media (min-width: 768px) {
      grid-template-columns: repeat(2, 1fr);
      grid-gap: 100px;
    }
  }
}
</style>
