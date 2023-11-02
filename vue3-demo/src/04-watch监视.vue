<script setup>
import { ref, watch } from 'vue';
// 准备数据
const count = ref(0)
const nickName = ref("张三")

// 方法-修改数据
const changeCount = () => {
    count.value++
}
const changeNickName = () => {
    nickName.value = "李四"
}

// 监听数据变化
// (1)监听单个数据变化
// watch(count, (newValue, oldValue) => {
//     console.log(newValue, oldValue);
// })
// 监听多个数据变化
// watch(
//     [count,nickName],
//     // ([newcount,newnickName],[oldcount,oldnickName])=>{
//     //     console.log("新值："+[newcount,newnickName]);
//     //     console.log("旧值："+[oldcount,oldnickName]);
//     // }
//     (newArr,oldArr) => {
//         console.log(newArr,oldArr);
//     })


// 立刻执行
// watch(count, (newValue, oldValue) => {
//     console.log(newValue, oldValue);
// },{
//     immediate:true // 一进页面立刻执行
// })

//  -----------------------------------------------

// 深度监视
// 1、数据
const userInfo = ref({
    name:'张三',
    age:18
})
// 2、方法
const setuserInfo = () =>{
    userInfo.value.age++
}
// 3、监视
// watch(userInfo,(newValue)=>{
//     console.log(newValue);
//     // console.log(oldValue);
// },{
//     // immediate:true,
//     deep:true
// }) 

// 4、精确监视
watch(()=>userInfo.value.age,(newValue,oldValue)=>{
    console.log(newValue,oldValue);
})


</script>

<template>
    <div>
        <div>序号：{{ count }}</div>
        <button @click="changeCount">修改序号</button>
        <div>昵称：{{ nickName }}</div>
        <button @click="changeNickName">修改昵称</button>
        <div>-----------------------------------</div>
        <div>{{ userInfo }}</div>
        <button @click="setuserInfo">修改age</button>
    </div>
</template>