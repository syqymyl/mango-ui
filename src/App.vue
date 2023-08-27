<template>
  <div>
    <Row :gutter="20">
      <Col>1</Col>
      <Col>2</Col>
    </Row>
    <Row :gutter="20">
      <Col>1</Col>
      <Col>2</Col>
      <Col>3</Col>
    </Row>
    <Row :gutter="20">
      <Col>1</Col>
      <Col>2</Col>
      <Col>3</Col>
      <Col>4</Col>
    </Row>
    <Row :gutter="20">
      <Col :span="2">1</Col>
      <Col :span="22">11</Col>
    </Row>
    <Row :gutter="20">
      <Col :span="2" :offset="2">1</Col>
      <Col :span="20">11</Col>
    </Row>
    <Row :gutter="20">
      <Col :span="2">1</Col>
      <Col :span="20" :offset="2">11</Col>
    </Row>
    <Row :gutter="20">
      <Col :span="4">1</Col>
      <Col :span="4" :offset="4">11</Col>
      <Col :span="6" :offset="6">11</Col>
    </Row>
  </div>
</template>

<script>
import Row from './component/Row.vue'
import Col from './component/Col.vue'
export default {
  name: 'App',
  components: { Row, Col },
}
</script>
