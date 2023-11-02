<script setup>
const count = 999
const sayHi = () => {
    console.log("hello");
}
defineExpose({
    count,
    sayHi
})

</script>

<template>
    <div>
        我是测试组件 - {{ count }}
        <button @click="sayHi">打招呼</button>
    </div>
</template>