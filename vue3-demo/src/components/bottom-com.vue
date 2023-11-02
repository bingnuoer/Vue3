<script setup>
// 跨层级接受数据：普通数据
import { inject } from 'vue';
const themeColor = inject('theme-color')
const newCount1 = inject('count1')
// 接收方法
const changeFn = inject('changeFn')

const clickFn = () => {
    changeFn(1000)
}
</script>

<template>
    <h3>我是底层组件-{{ themeColor }} - {{ newCount1 }}</h3>
    <button @click="clickFn">修改数值</button>
</template>