<template>
  <button type="button">
    <slot />
  </button>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: ['class-name'],
})
</script>

<style lang="scss" scoped>
button {
  overflow: hidden;
  margin-right: 10px;
  &:last-child {
    margin-right: 0;
  }
  display: flex;
  justify-content: center;
  align-items: center;
  height: 30px;
  &.t_icon {
    width: 36px;
    height: 36px;
    border: 0;
    font-size: 30px;
  }
}
</style>
