<template>
  <div
    class="col"
    :class="[span && `col-${span}`, offset && `offset-${offset}`]"
  >
    <div style="border: 1px solid green; height: 100px">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Col',
  props: {
    span: {
      type: Number,
    },
    offset: {
      type: Number,
    },
    gutter: {
      type: Number,
      default: 0,
    },
  },
  created() {
    console.log('col created')
  },
  mounted() {
    console.log('col mounted')
  },
}
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
