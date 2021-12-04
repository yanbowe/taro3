<template>
  <view class="page-body">
    <view class="page-section">
      <text>地区选择器{{ index }} </text>
      <view>
        <picker mode="selector" :range="selector" @change="onChange" :value="index">
          <view class="picker"> 当前选择：{{ selectorChecked }} </view>
        </picker>
      </view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import { ref } from "vue";
const index = ref(0);
const selectorChecked = ref("美国");

const selector = ["美国", "中国", "巴西", "日本"];
function onChange(e) {
  selectorChecked.value = selector[e.detail.value];
  index.value = selector.findIndex((v) => v === selectorChecked.value);
}
</script>
