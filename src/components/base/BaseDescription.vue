<template>
  <div class="base-description"><slot></slot></div>
</template>
<script>
export default {
  name: "BaseDescription",
};
</script>
<style lang="scss">
.base-description {
  p {
    font-size: 14px;
    font-weight: 100;
    line-height: 180%;

    @media (min-width: 768px) {
      font-size: 16px;
    }
  }
}
</style>
