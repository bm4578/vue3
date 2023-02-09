<template>

  <h2>子组件</h2>
  <h1>{{ msg }}</h1>
  <hr>
</template>


<script setup>
import {defineProps} from 'vue'
//接收父传的数据
defineProps({
  msg:{
    type:String,
    default:"测试"
  }
})
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
