<template>

  <h2>子组件</h2>
  <h1>{{ msg }}</h1>
  <hr>
  <button @click="button">子组件</button>
</template>


<script setup>
import {defineProps, ref} from 'vue'
//接收父传的数据
defineProps({
  msg:{
    type:String,
    default:"测试"
  }
})




//子传父
// 使用defineEmits创建名称，接受一个数组
const emit = defineEmits(['button'])

let data = ref("子元素")
//定义要给父亲传递的数据
const button =()=>{
  //传递给父组件
  emit('clickChild',data)
}
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
