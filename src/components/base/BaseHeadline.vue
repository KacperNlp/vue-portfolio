<template>
  <div class="base-headline">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: "BaseHeadline",
};
</script>
<style lang="scss" scoped>
.base-headline {
  h1,
  h2,
  h3 {
    font-weight: 700;
    color: #d9d9d9;
  }

  h1 {
    font-size: 64px;

    @media (min-width: 768px) {
      font-size: 96px;
    }
  }

  h2 {
    font-size: 48px;

    @media (min-width: 768px) {
      font-size: 64px;
    }
  }

  h3 {
    font-size: 24px;

    @media (min-width: 768px) {
      font-size: 32px;
    }
  }
}
</style>
