<template>
  <label>
    <input type="radio">
    <slot>单选框</slot>
  </label>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
// import { ButtonType, ButtonSize } from './radio.ts'

@Component
export default class Radio extends Vue {
  @Prop(String) type !: string
  @Prop(String) size !: string

  private selfClick() {
    this.$emit('click')
  }

  private data() {
    return {
      // selfType: ButtonType[this.type || 'default'],
      // selfSize: ButtonSize[this.size || 'medium'],
    }
  }
}
</script>

<style lang="scss" scoped>
@import './radio.scss'
</style>
