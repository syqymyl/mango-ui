<template>
  <div
    class="row"
    :style="{ marginLeft: -gutter / 2 + 'px', marginRight: -gutter / 2 + 'px' }"
  >
    <slot></slot>
  </div>
</template>

<script>
import { onMounted } from 'vue'
export default {
  name: 'Row',
  props: {
    gutter: {
      type: Number,
      default: 0,
    },
  },
  setup(props, context) {
    console.log(context.slots.default())
    const defaults = context.slots.default()
    defaults.forEach((vm) => {
      vm.gutter = props.gutter
    })
  },
  // created() {
  //   console.log('row created')
  // },
  // mounted() {
  //   console.log('row mounted')
  //   console.log(this.$refs)
  //   this.$children.forEach((vm) => {
  //     vm.gutter = this.gutter
  //   })
  // },
}
</script>

<style lang="scss" scoped>
.row {
  display: flex;
}
</style>
