<template>
  <!-- <Layout class="layout1">
    <Header class="demo"></Header>
    <Content class="demo"></Content>
    <Footer class="demo"></Footer>
  </Layout> -->
  <Layout class="layout2">
    <Header class="demo">Header</Header>
    <Layout>
      <Sider class="demo">Sider</Sider>
      <Content class="demo">Content</Content>
    </Layout>
    <Footer class="demo">Footer</Footer>
  </Layout>
</template>

<script>
import Layout from './component/Layout.vue'
import Sider from './component/Sider.vue'
import Header from './component/Header.vue'
import Content from './component/Content.vue'
import Footer from './component/Footer.vue'
export default {
  name: 'App',
  components: { Layout, Sider, Header, Content, Footer },
}
</script>

<style lang="scss" scoped>
.layout2 {
  height: 100vh;
}
.demo {
  border: 1px solid black;
  background-color: #acacef;
  min-height: 100px;
}
</style>
