<template>
  <div class="hello">
    <span>
      {{ msg }}
    </span>
    <ts-button class="my-btn" />
  </div>
</template>

<script lang="ts">
import Button from '@components/button/Button.vue'
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component({
  components: {
    'ts-button': Button
  }
})
export default class HelloWorld extends Vue {
  @Prop() public msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .my-btn{
    width: 60px;
  }
</style>
