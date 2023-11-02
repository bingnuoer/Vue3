<script setup>
    import { ref,computed } from 'vue';
    const arr = ref([1,2,3,4,5])

    // 计算属性，过滤数组
    const computedArr = computed(() => {
        return arr.value.filter(item => item>2)
    })

    // 方法,操作原数组
    const addFn = () => {
        // 给数组增加数据
        arr.value.push(666)
    }


</script>

<template>
    <div>
        <div>原始数据：{{ arr }}</div>
        <div>过滤后的数据： {{ computedArr }}</div>
        <button @click="addFn">修改</button>
    </div>
</template>