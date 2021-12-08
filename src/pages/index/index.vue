<template>
  <view class="page-body">
    <nut-collapse v-model:active="activeName" :accordion="true" icon="down-arrow">
      <nut-collapse-item :title="title1" :name="1">
        <view> 基于京东设计语言体系，构建场景</view>
      </nut-collapse-item>
      <nut-collapse-item :title="title2" :name="2" :sub-title="subTitle">
        提高界⾯的模块化通用程度
      </nut-collapse-item>
      <nut-collapse-item :title="title3" :name="3">
        采用组合式 API Composition 语法重构，结构清晰，功能模块化
      </nut-collapse-item>
    </nut-collapse>
  </view>
</template>

<script lang="ts" setup>
import { ref, reactive } from "vue";
const activeName = ref(1);
const subTitle = "副标题";
const title = reactive({
  title1: "标题1",
  title2: "标题2",
  title3: "标题3",
});
</script>
