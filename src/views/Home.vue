<template>
  <div class="home">
    hello everybody, 初次见面，请多关照
    <HelloWorld msg="1" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloWorld from '@components/HelloWorld.vue' // @ is an alias to /src
import Header from '@components/Header.vue'

@Component({
  components: {
    HelloWorld,
    Header
  }
})
export default class Home extends Vue {}
</script>
