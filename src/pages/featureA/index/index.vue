<template>
  <NumberDisplay />
  <NumberSubmit />
  <div class="ellipsis-test ellipsis">
    测试超行省略
  </div>
</template>
<script lang="ts" setup>
import { useDidShow, usePullDownRefresh } from '@/hooks/life'
import NumberDisplay from '@/components/NumberDisplay.vue'
import NumberSubmit from '@/components/NumberSubmit.vue'

import Taro from '@tarojs/taro'
useDidShow(() => {
  console.log('onShow')
})
usePullDownRefresh(() => {
  console.log('onPullDownRefresh')
  Taro.vibrateShort()
  Taro.stopPullDownRefresh()
})
</script>

<style lang="scss">
.ellipsis-test {
  width: 50px;
}
</style>
