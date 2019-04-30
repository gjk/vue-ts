<template>
  <button class="ts-button" :type="selfType" :size="selfSize" @click="selfClick">
    <i
      v-if="iconPrefix"
      :class="iconPrefix ? iconPrefix : ''"
    />
    <slot>提交</slot>
    <i
      v-if="iconSuffix"
      :class="iconSuffix ? iconSuffix : ''"
    />
  </button>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import { ButtonType, ButtonSize } from './button.ts'

@Component
export default class Button extends Vue {
  // 文字前按钮样式
  @Prop(String) iconPrefix !: string
  @Prop(String) iconSuffix !: string
  @Prop(String) type !: string
  @Prop(String) size !: string

  private selfClick() {
    this.$emit('click')
  }

  private data() {
    return {
      selfType: ButtonType[this.type || 'default'],
      selfSize: ButtonSize[this.size || 'medium'],
    }
  }
}
</script>

<style lang="scss" scoped>
@import './button.scss'
</style>
