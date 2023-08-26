<template>
  <div
    class="row"
    :style="{ marginLeft: -gutter / 2 + 'px', marginRight: -gutter / 2 + 'px' }"
  >
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Row',
  props: {
    gutter: {
      type: Number,
      default: 0,
    },
  },
  created() {
    console.log('row created')
  },
  mounted() {
    console.log('row mounted')
    console.log(this.$children)
    // this.$children.forEach((vm) => {
    //   vm.gutter = this.gutter
    // })
  },
}
</script>

<style lang="scss" scoped>
.row {
  display: flex;
}
</style>
