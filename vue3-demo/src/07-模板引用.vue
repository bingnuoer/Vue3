<script setup>
import TestCom from "@/components/test-com.vue"
// 1.调用ref 生成ref对象
// 2.绑定ref-要获取的值
// 3. .value访问ref值
import { onMounted, ref } from "vue"

const inp = ref(null)

// 生命周期钩子 Dom渲染完毕聚焦
onMounted(()=>{
    // console.log(inp.value);
    // inp.value.focus()
})

// 点击按钮聚焦
const getFacus = () => {
    inp.value.focus()   
}

// ------------------------------------
const testRef = ref(null)
const getCom = () => {
    console.log(testRef.value);
    // 获取组件-里的方法
    console.log(testRef.value.count);
    testRef.value.sayHi()
}


</script>

<template>
    <div>
        <input ref="inp" type="text">
        <button @click="getFacus">点击让输入框聚焦</button>
    </div>
    <TestCom ref="testRef"></TestCom>
    <button @click="getCom">获取组件</button>
</template>