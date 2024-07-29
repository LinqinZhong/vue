<template>
  <div class="home">
    <!-- 通过v-if控制,当需要显示的时候才去加载 -->
    <button @click="showComponent = true">显示组件</button>
    <AComponent v-if="showComponent" />
  </div>
</template>

<script lang="ts" setup>
import { defineAsyncComponent, ref, } from 'vue';
const showComponent = ref<boolean>(false)

/**
 * 同步加载组件
 */
// import AComponent from '@/components/AComponet.vue'

/**
 * 异步加载组件
 */
const AComponent = defineAsyncComponent(() => {
  return import('@/components/AComponet.vue');
})
</script>
