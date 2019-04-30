<template>
  <div id="app">
    <my-header></my-header>
    <div class="main fix">
      <my-left></my-left>
      <div id="main">
        <router-view />
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
  }
}
#main{
  float: left;
  margin: 60px 0 0 30px;
}
</style>
