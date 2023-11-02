<script setup>
// 子组件
// 宏定义 props接收数据
const props = defineProps({
    car: String,
    money:Number
})
// 宏定义 emit传送数据
const emit = defineEmits(['changeMoney'])
console.log(props.car,props.money); //宝马车
const buy = () => {
    // emit触发事件
    emit("changeMoney",5);
}
</script>

<template>
    <div class="son">我是子组件 - {{ car }} - {{ money}}
    <button @click="buy">花钱</button>
    </div>
</template>

<style scoped>
.son {
    border: 1px solid #000;
    padding: 30px;
}
</style>