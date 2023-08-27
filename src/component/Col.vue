<template>
  <div
    class="col"
    :class="[span && `col-${span}`, offset && `offset-${offset}`]"
    :style="{ paddingLeft: gutter / 2 + 'px', paddingRight: gutter / 2 + 'px' }"
  >
    <div style="border: 1px solid green; height: 100px">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import { defineComponent, inject } from 'vue'
export default defineComponent({
  props: {
    span: {
      type: Number,
    },
    offset: {
      type: Number,
    },
  },
  setup() {
    const gutter = inject('gutter')
    return {
      gutter,
    }
  },
})
</script>

<style lang="scss" scoped>
.col {
  height: 100px;
  width: 50%;

  $class-prefix: col-;
  @for $n from 1 through 24 {
    &.#{$class-prefix}#{$n} {
      width: calc($n/24) * 100%;
    }
  }
  $class-prefix: offset-;
  @for $n from 1 through 24 {
    &.#{$class-prefix}#{$n} {
      margin-left: calc($n/24) * 100%;
    }
  }
}
</style>
