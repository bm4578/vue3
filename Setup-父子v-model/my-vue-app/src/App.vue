<template>
  <h1>父组件</h1>
  <HelloWorld v-model:msg='msg' />
</template>


<script setup>
import HelloWorld from './components/HelloWorld.vue'
import {ref} from "vue";

let msg = ref("父数据")
</script>
