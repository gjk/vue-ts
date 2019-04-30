<template>
  <div>
    <h2>普通按钮</h2>
    <div>
      <ts-button>普通按钮</ts-button>
      <ts-button type="primary">普通按钮</ts-button>
      <ts-button type="success">成功按钮</ts-button>
      <ts-button type="warning">提示按钮</ts-button>
      <ts-button type="danger">警告按钮</ts-button>
      <ts-button type="info">信息按钮</ts-button>
      <ts-button type="text">文本按钮</ts-button>
    </div>
    <h2>小号按钮</h2>
    <div>
      <ts-button size="small">小号按钮</ts-button>
      <ts-button size="small" type="primary">小号按钮</ts-button>
      <ts-button size="small" type="success">小号按钮</ts-button>
      <ts-button size="small" type="warning">小号按钮</ts-button>
      <ts-button size="small" type="danger">小号按钮</ts-button>
      <ts-button size="small" type="info">小号按钮</ts-button>
      <ts-button size="small" type="text">小号按钮</ts-button>
    </div>
    <h2>最小号按钮</h2>
    <div>
      <ts-button size="mini">最小号按钮</ts-button>
      <ts-button size="mini" type="primary">最小号按钮</ts-button>
      <ts-button size="mini" type="success">最小号按钮</ts-button>
      <ts-button size="mini" type="warning">最小号按钮</ts-button>
      <ts-button size="mini" type="danger">最小号按钮</ts-button>
      <ts-button size="mini" type="info">最小号按钮</ts-button>
      <ts-button size="mini" type="text">最小号按钮</ts-button>
    </div>
    <h2>禁用状态</h2>
    <div>
      <ts-button disabled>禁用状态</ts-button>
      <ts-button disabled type="primary">普通按钮</ts-button>
      <ts-button disabled type="success">成功按钮</ts-button>
      <ts-button disabled type="warning">提示按钮</ts-button>
      <ts-button disabled type="danger">警告按钮</ts-button>
      <ts-button disabled type="info">信息按钮</ts-button>
      <ts-button disabled type="text">文本按钮</ts-button>
    </div>
    <h2>前缀、后缀、loading</h2>
    <div>
      <ts-button type="primary"><i>abc</i>普通按钮<i>cba</i></ts-button>
    </div>

  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'
import Button from '@components/button/Button.vue'
@Component({
  components: {
    'ts-button': Button
  }
})
export default class ButtonPage extends Vue {

}
</script>

<style lang="scss" scoped>

</style>
