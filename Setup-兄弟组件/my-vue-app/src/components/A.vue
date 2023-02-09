<template>
  <div class="app">
    <h1>A组件</h1>
    <button @click="btn"> A</button>
  </div>
</template>

<script setup>
import emitter from '../plugins/bus'
import {ref} from 'vue'

let A = ref("这是A组件的数据")

const btn=()=>{
  emitter.emit('fn',A)
}
</script>

<style scoped>
.app{
  width: 200px;
  height: 200px;
  border: #1a1a1a 1px solid;
}
</style>