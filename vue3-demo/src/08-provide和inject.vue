<script setup>
import centerCom from './components/center-com.vue';
// 1.爷爷-孙子 跨层级：传递普通数据
import { provide, ref } from 'vue';
provide('theme-color', 'pink')

// 2.- 传响应式数据
const count = ref(100)
provide('count1', count)

setTimeout(() => {
    count.value = 500
},500)

// 3.传递方法-修改数据
provide('changeFn',(newCount) => {
    count.value = newCount
})
</script>

<template>
    <h1>我是顶层组件</h1>
    <centerCom></centerCom>
</template>