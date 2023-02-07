<template>
  <button class="bar" :class="{ active: isNavActive }" @click="openNav">
    <span></span>
  </button>
</template>
<script>
export default {
  name: "BaseBar",
  data() {
    return {
      isNavActive: false,
    };
  },

  methods: {
    openNav() {
      this.isNavActive = !this.isNavActive;
    },
  },
};
</script>
<style lang="scss">
.bar {
  position: fixed;
  top: 25px;
  right: 20px;
  height: 27px;
  width: 34px;
  z-index: 99;
  background: transparent;
  border: none;
  outline: transparent;
  overflow: hidden;

  @media (min-width: 1280px) {
    display: none;
  }

  span {
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-50%);
    width: 100%;
    height: 1px;
    background: #d9d9d9;
    transition: 0.3s;
  }

  &::before,
  &::after {
    content: "";
    position: absolute;
    left: 0;
    width: 100%;
    height: 1px;
    background: #d9d9d9;
    transition: 0.3s;
    transform-origin: center left;
  }

  &::before {
    top: 0;
  }

  &::after {
    top: calc(100% - 1px);
  }

  &.active {
    span {
      left: -105%;
    }

    &::before {
      transform: rotate(45deg) translate(2px, 1px);
    }

    &::after {
      transform: rotate(-45deg) translate(1px, 1px);
    }
  }

  &:hover {
    span,
    &::before,
    &::after {
      background: #cd5888;
    }
  }
}
</style>
