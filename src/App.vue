<template>
  <Popover>
    <template slot="content">
      <div>popover气泡内容</div>
    </template>
    <button>click</button>
  </Popover>
</template>

<script>
import Popover from './component/Popover.vue'
export default {
  name: 'App',
  components: { Popover },
}
</script>

<style lang="scss" scoped></style>
