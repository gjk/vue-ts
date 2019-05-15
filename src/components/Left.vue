<template>
  <aside class="left-menu">
    <ul>
      <li><router-link to="buttonpage">按钮</router-link></li>
      <li><router-link to="radiopage">单选按钮</router-link></li>
      <li><a href="#">测试页2</a></li>
    </ul>
  </aside>
</template>

<style lang="scss" scoped>
.left-menu{
  float: left;
  width: 230px;
  box-shadow: 1px 0 0 rgba(0,0,0,0.25);
}
</style>
