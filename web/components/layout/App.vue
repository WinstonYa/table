<template>
  <router-view :asyncData="asyncData" />
</template>

<script lang="ts">
// 在这里可以进行一些全局组件的注册逻辑

import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
Vue.use(ElementUI);
export default {
  props: ['asyncData'],
};
</script>

<style lang="less">
@import '@/common.less';
</style>
