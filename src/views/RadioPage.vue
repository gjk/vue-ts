<template>
  <div>
    <ts-radio>选项一</ts-radio>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'
import Radio from '@components/radio/Radio.vue'
@Component({
  components: {
    'ts-radio': Radio
  }
})
export default class RadioPage extends Vue {

}
</script>