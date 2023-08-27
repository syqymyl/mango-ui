<template>
  <div
    class="row"
    :style="{ marginLeft: -gutter / 2 + 'px', marginRight: -gutter / 2 + 'px' }"
  >
    <slot></slot>
  </div>
</template>

<script>
import { computed, provide } from 'vue'
export default {
  name: 'Row',
  props: {
    gutter: {
      type: Number,
      default: 0,
    },
  },
  setup(props, context) {
    provide(
      'gutter',
      computed(() => props.gutter)
    )
  },
}
</script>

<style lang="scss" scoped>
.row {
  display: flex;
}
</style>
