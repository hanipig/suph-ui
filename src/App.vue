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
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="medium"></suph-button> -->
      <suph-button size="medium">默认按钮</suph-button>
      <suph-button type="primary" size="medium">默认按钮</suph-button>
      <suph-button type="success" size="medium">默认按钮</suph-button>
      <suph-button type="danger" size="medium">默认按钮</suph-button>
      <suph-button type="info" size="medium">默认按钮</suph-button>
      <suph-button type="warning" size="medium">默认按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="small"></suph-button> -->
      <suph-button size="small">默认按钮</suph-button>
      <suph-button type="primary" size="small">默认按钮</suph-button>
      <suph-button type="success" size="small">默认按钮</suph-button>
      <suph-button type="danger" size="small">默认按钮</suph-button>
      <suph-button type="info" size="small">默认按钮</suph-button>
      <suph-button type="warning" size="small">默认按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="mini"></suph-button> -->
      <suph-button size="mini">默认按钮</suph-button>
      <suph-button type="primary" size="mini">默认按钮</suph-button>
      <suph-button type="success" size="mini">默认按钮</suph-button>
      <suph-button type="danger" size="mini">默认按钮</suph-button>
      <suph-button type="info" size="mini">默认按钮</suph-button>
      <suph-button type="warning" size="mini">默认按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button></suph-button> -->
      <suph-button :disabled="isDisabled">默认按钮</suph-button>
      <suph-button type="primary" :disabled="isDisabled">默认按钮</suph-button>
      <suph-button type="success" :disabled="isDisabled">默认按钮</suph-button>
      <suph-button type="danger" :disabled="isDisabled">默认按钮</suph-button>
      <suph-button type="info" :disabled="isDisabled">默认按钮</suph-button>
      <suph-button type="warning" :disabled="isDisabled">默认按钮</suph-button>
    </div>
    <div class="demo-tr">
      <!-- <suph-button size="small"></suph-button> -->
      <suph-button size="mini" :round="round">圆形按钮</suph-button>
      <suph-button type="primary" size="small" :round="round">圆形按钮</suph-button>
      <suph-button type="success" size="medium" :round="round">圆形按钮</suph-button>
      <suph-button type="danger" :round="round">圆形按钮</suph-button>
      <suph-button type="info" :round="round">圆形按钮</suph-button>
      <suph-button type="warning" :round="round">圆形按钮</suph-button>
    </div>
    <div class="demo-tr">
      <suph-button plain="plain">朴素按钮</suph-button>
      <suph-button type="primary" plain="plain">朴素按钮</suph-button>
      <suph-button type="success" plain="plain">朴素按钮</suph-button>
      <suph-button type="danger" plain="plain">朴素按钮</suph-button>
      <suph-button type="info" plain="plain">朴素按钮</suph-button>
      <suph-button type="warning" plain="plain">朴素按钮</suph-button>
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