<template>
  <button v-bind:type="type" :class="{ btn: true, 'btn--outlined': outlined }">
    <slot></slot>
  </button>
</template>

<script>
// import { Linter } from "eslint";

export default {
  name: "ButtonApp",
  props: {
    type: {
      type: String,
      default: "button",
    },
    outlined: {
      type: Boolean,
      default: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  display: inline-block;
  font-size: 18px;
  background: #ff662d;
  color: #fff;
  cursor: pointer;
  min-width: 220px;
  border: 1px solid transparent;
  padding: 8px 15px;
  &--outlined {
    background: transparent;
    color: #ff662d;
    border: 1px solid #ff662d;
  }
}
</style>
