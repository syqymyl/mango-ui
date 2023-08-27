<template>
  <div class="col" :class="colClass" :style="colStyle">
    <div style="border: 1px solid red; height: 100px">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import { computed, defineComponent, inject } from 'vue'
export default defineComponent({
  props: {
    span: {
      type: Number,
    },
    offset: {
      type: Number,
    },
  },
  setup(props, context) {
    let { span, offset } = props
    const colClass = computed(() => {
      return [span && `col-${span}`, offset && `offset-${offset}`]
    })

    const gutter = inject('gutter')
    const colStyle = computed(() => {
      return { paddingLeft: gutter / 2 + 'px', paddingRight: gutter / 2 + 'px' }
    })
    return {
      colClass,
      colStyle,
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
