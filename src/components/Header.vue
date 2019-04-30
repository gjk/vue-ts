<template>
  <div id="header">
    <a class="logo" href="#">
      <img
        alt="Vue logo"
        src="@assets/logo.png"
      >
      Vue Administration
    </a>
    <ul class="menu">
      <li>欢迎你，</li>
      <li>退出</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import { mapGetters } from 'vuex'

@Component
export default class Header extends Vue {

}

</script>

<style scoped lang="scss">
  #header{
    position: fixed;
    width: 100%;
    top: 0;
    height: 40px;
    padding: 10px 60px;
    text-align: left;
    background-color: rgba(255,255,255,0.4);
    box-shadow: 0 0 1px rgba(0,0,0,0.25);
    transition: background-color 0.3s ease-in-out;
    .logo{
      font-size: 1.5em;
      line-height: 40px;
      color: #2c3e50;
      font-weight: 500;
      img{
        display: inline-block;
        width: 50px;
        height: 40px;
      }
    }
    .menu{
      position: fixed;
      list-style-type: none;
      right: 30px;
      top: 10px;
      height: 40px;
      line-height: 40px;

      li {
        display: inline-block;
        position: relative;
        margin: 0 0.6em;
        a{
          text-decoration: none;
          color: #34495e;
          padding-bottom: 3px;
          white-space: nowrap;
          border-bottom: 3px solid #42b983;
        }
      }
    }
  }
</style>
