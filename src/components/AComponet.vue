<template>
    <div>我是一个异步组件</div>
</template>
<script lang="ts">
console.log('我被执行了');
export default {
    created() {
        console.log('我被创建了');
    },
    mounted() {
        console.log('我被挂载了');
    }
}
</script>