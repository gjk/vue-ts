<template>
  <div id="app">
    <my-header></my-header>
    <div class="main fix">
      <div class="flex-item-left">
        <my-left></my-left>
      </div>
      <div id="main" class="fix">
        <div class="main-container">
          <router-view />
        </div>
        <div class="copyright">我是 copyright 潘多拉备案号：潘审MV900000019</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Left from '@components/Left.vue'
import Header from '@components/Header.vue'
import { Component } from 'vue-property-decorator'
import '@assets/css/reset.scss'
import '@assets/css/common.scss'

@Component({
  components: {
    'my-left': Left,
    'my-header': Header
  }
})
export default class AppClass extends Vue {

}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  .main{
    margin-top: 60px;
    clear: both;

    display: flex;

    .flex-item-left{
      height: auto;
      align-items: stretch;
      background-color: var(--light);
    }
  }

}
#main{
  float: left;
  display: flex;
  flex-direction: column;

  .main-container{
    margin: 60px 0 0 30px;
    align-self: flex-start;
  }
  .copyright{
    width: 100%;
    margin: 0 auto;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: var(--light);
    background-color: var(--gray-dark);
    align-self: flex-end;
  }
}
</style>
