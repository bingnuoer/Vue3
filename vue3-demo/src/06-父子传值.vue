<script setup>
// 父传子
// 导入组件
import sonCom from "@/components/son-com.vue"
// 响应式传值
import { ref } from "vue"

const money = ref(100)
const getMoney = () => {
    money.value += 10
}
const changeFn = (newMoney) => {
    money.value = newMoney
}
</script>

<template>
    <div>
        <h1>
            父组件 - {{ money }}
            <button @click="getMoney">挣钱</button>
        </h1>
        <!-- 使用组件 -->
        <!-- 传数据 -->
        <sonCom 
        car="宝马车" 
        :money="money"
        @changeMoney="changeFn">
        
        </sonCom>
    </div>
</template>