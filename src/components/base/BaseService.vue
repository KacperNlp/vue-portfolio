<template>
  <div class="base-service">
    <div class="base-service-icon"></div>
    <base-headline
      ><h3 class="base-service-headline">{{ headline }}</h3></base-headline
    >
    <base-description
      ><p class="base-service-description">
        {{ description }}
      </p></base-description
    >
  </div>
</template>
<script>
import BaseDescription from "./BaseDescription.vue";
import BaseHeadline from "./BaseHeadline.vue";

export default {
  name: "BaseService",
  components: { BaseHeadline, BaseDescription },

  props: {
    headline: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: false,
    },
  },
};
</script>
<style lang="scss">
.base-service {
  display: flex;
  flex-direction: column;

  &-icon {
    width: 50px;
    height: 50px;
    margin-bottom: 18px;
    background: #cd5888;

    @media (min-width: 768px) {
      margin-bottom: 26px;
    }
  }

  &-headline {
    margin-bottom: 12px;
  }
}
</style>
