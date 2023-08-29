<template>
  <div class="popover" @click="x">
    <slot name="content" v-if="visible"></slot>
    <slot></slot>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Popover',
  setup() {
    const visible = ref(false)
    const x = () => {
      visible.value = !visible.value
    }
    return { visible, x }
  },
}
</script>

<style lang="scss" scoped>
.popover {
  display: inline-block;
  vertical-align: top;
}
</style>
