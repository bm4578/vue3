<template>
  <div class="app">
    <h1>B组件</h1>
    <h1>{{B}}</h1>
  </div>
</template>

<script setup>
import emitter from '../plugins/bus'
import {onBeforeMount, ref} from 'vue'

let B = ref('')
onBeforeMount(()=>{
  emitter.on('fn',e=>{
    B.value = e.value
  })
})

</script>

<style scoped>
.app{
  width: 600px;
  height: 200px;
  border: #1a1a1a 1px solid;
}
</style>