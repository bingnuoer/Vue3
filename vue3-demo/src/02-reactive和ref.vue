<script setup>
// import { reactive } from 'vue';
import { ref } from 'vue';

// reactive会返回一个响应式对象数据
// const message = reactive({
//   count:100
// })
// const logCount = ()=> {
//   message.count++
// }

// ref 简单/复杂数据类型，返回对象数据
// const count = ref(0)
// // console.log(count);
// const setCount = () => {
//   count.value++
// }

const message = ref({
  count:100,
  price:999
})
const setCount = () => {
  message.value.count++
}
</script>

<template>
  <h1>{{ message.count }}</h1>
  <h2>{{ message.price }}</h2>
  <button @click="setCount">+1</button>

</template>

