<template>
  <div id="app">
    <div class="demo-tr">
      <!-- <suph-button></suph-button> -->
      <suph-button>默认按钮</suph-button>
      <suph-button type="primary">默认按钮</suph-button>
      <suph-button type="success">默认按钮</suph-button>
      <suph-button type="danger">默认按钮</suph-button>
      <suph-button type="info">默认按钮</suph-button>
      <suph-button type="warning">默认按钮</suph-button>
      <suph-button type="text">文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="medium"></suph-button> -->
      <suph-button size="medium">默认按钮</suph-button>
      <suph-button type="primary" size="medium">默认按钮</suph-button>
      <suph-button type="success" size="medium">默认按钮</suph-button>
      <suph-button type="danger" size="medium">默认按钮</suph-button>
      <suph-button type="info" size="medium">默认按钮</suph-button>
      <suph-button type="warning" size="medium">默认按钮</suph-button>
      <suph-button type="text" size="medium">文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="small"></suph-button> -->
      <suph-button size="small">默认按钮</suph-button>
      <suph-button type="primary" size="small">默认按钮</suph-button>
      <suph-button type="success" size="small">默认按钮</suph-button>
      <suph-button type="danger" size="small">默认按钮</suph-button>
      <suph-button type="info" size="small">默认按钮</suph-button>
      <suph-button type="warning" size="small">默认按钮</suph-button>
      <suph-button type="text" size="small">文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="mini"></suph-button> -->
      <suph-button size="mini">默认按钮</suph-button>
      <suph-button type="primary" size="mini">默认按钮</suph-button>
      <suph-button type="success" size="mini">默认按钮</suph-button>
      <suph-button type="danger" size="mini">默认按钮</suph-button>
      <suph-button type="info" size="mini">默认按钮</suph-button>
      <suph-button type="warning" size="mini">默认按钮</suph-button>
      <suph-button type="text" size="mini">文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button></suph-button> -->
      <suph-button disabled>默认按钮</suph-button>
      <suph-button type="primary" disabled>默认按钮</suph-button>
      <suph-button type="success" disabled>默认按钮</suph-button>
      <suph-button type="danger" disabled>默认按钮</suph-button>
      <suph-button type="info" disabled>默认按钮</suph-button>
      <suph-button type="warning" disabled>默认按钮</suph-button>
      <suph-button type="text" disabled>文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="small"></suph-button> -->
      <suph-button size="mini" round>圆形按钮</suph-button>
      <suph-button type="primary" size="small" round>圆形按钮</suph-button>
      <suph-button type="success" size="medium" round>圆形按钮</suph-button>
      <suph-button type="danger" round>圆形按钮</suph-button>
      <suph-button type="info" round>圆形按钮</suph-button>
      <suph-button type="warning" round>圆形按钮</suph-button>
      <suph-button type="text" round>文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <suph-button plain>朴素按钮</suph-button>
      <suph-button type="primary" plain>朴素按钮</suph-button>
      <suph-button type="success" plain>朴素按钮</suph-button>
      <suph-button type="danger" plain>朴素按钮</suph-button>
      <suph-button type="info" plain>朴素按钮</suph-button>
      <suph-button type="warning" plain>朴素按钮</suph-button>
      <suph-button type="text" plain>文本按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button></suph-button> -->
      <suph-button @click="handleClick">点击事件</suph-button>
      <suph-button @click="handleClick" disabled>点击事件</suph-button>
    </div>
  </div>
</template>

<script>
import SuphButton from './components/Button.vue';

export default {
  name: 'App',
  components: {
    SuphButton
  },
  data () {
    return {
      isDisabled: true,
      round: true
    }
  },
  methods: {
    handleClick (e) {
      console.log(e);
    }
  }
}
</script>

<style lang="less" scoped>
.demo-tr {
  margin-bottom: 8px;
  button {
    margin-right: 12px !important;
  }
}
</style>