<template>
  <div class="base-tile">{{ text }}</div>
</template>
<script>
export default {
  name: "BaseTile",
  props: {
    text: {
      type: String,
      required: true,
    },
  },
};
</script>
<style lang="scss">
.base-tile {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 70px;
  height: 70px;
  background: rgba(217, 217, 217, 0.1);
  transition: 0.3s;
  cursor: default;

  &:hover {
    transform: scale(1.1);
    color: #cd5888;
  }
}
</style>
