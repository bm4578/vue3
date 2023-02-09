<template>
  <!-- 子传父-->
    <HelloWorld @clickChild='changeHome' />
    <h2 >{{data}}</h2>
    <hr>
</template>


<script setup>
import HelloWorld from './components/HelloWorld.vue'
import {ref} from 'vue'
//定义子传父的元素
let data = ref("test")
const changeHome=(val)=>{
  data.value = val.value
}
</script>