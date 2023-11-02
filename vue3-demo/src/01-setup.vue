<!-- <script>
 export default {
  setup(){
    // console.log("这是setup",this);
    const message = "Hello Vue3"
    const logMessage = () => {
      console.log(message);
    }
    return {
      message,
      logMessage
    }
  },
  beforeCreate(){
    console.log("这是beforeCreate");
  }
 }
</script> -->

<!-- setup语法糖 -->
<script setup>
  const message = "这是message"
  const logMessage = () => {
    console.log(message);
  }

</script>

<template>
  <h1>{{ message }}</h1>
  <button @click="logMessage">点击</button>
</template>
