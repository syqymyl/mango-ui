<template>
  <!-- <Layout class="layout4">
    <Header class="demo"></Header>
    <Layout>
      <Sider class="demo"></Sider>
      <Content class="demo"></Content>
    </Layout>
    <Footer class="demo"></Footer>
  </Layout>
  <Layout class="layout">
    <Header class="demo"></Header>
    <Layout>
      <Sider class="demo"></Sider>
      <Content class="demo"></Content>
    </Layout>
    <Footer class="demo"></Footer>
  </Layout> -->
  <Layout class="layout4">
    <Sider class="demo"></Sider>
    <Layout>
      <Header class="demo"></Header>
      <Content class="demo"></Content>
      <Footer class="demo"></Footer>
    </Layout>
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
.layout4 {
  height: 100vh;
  background-color: #acacef;
}
.demo {
  border: 1px solid black;
  min-height: 100px;
}
.sider {
  width: 200px;
}
</style>
