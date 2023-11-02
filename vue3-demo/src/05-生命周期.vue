<script setup>
import { onMounted } from 'vue';

    // create
    const getCreate = () =>{
        setInterval(()=>{
            console.log("获取数据");
        },1000)
    }
    getCreate()

    // Mountedted 生命周期
    onMounted(()=>{
        console.log("mounted生命周期函数-逻辑1");
    })
    onMounted(()=>{
        console.log("mounted生命周期函数-逻辑2");
    })
</script>

<template>
    <div></div>
</template>