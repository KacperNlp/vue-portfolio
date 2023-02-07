<template>
  <div class="fixed-image-container">
    <img
      src="../../assets/kacper-photo.jpg"
      alt="Kacper Nalepa - Frontend Developer"
      class="fixed-image-container-image"
    />
  </div>
</template>
<script>
export default {
  name: "TheFixedImage",
};
</script>
<style lang="scss">
.fixed-image-container {
  &-image {
    width: 100%;
    height: 100%;
  }
}
</style>
