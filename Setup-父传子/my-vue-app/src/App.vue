<template>

<!--  父传子-->
  <div>
    <h2>父组件</h2>
  </div>
  <HelloWorld :msg='msg' />
</template>


<script setup>
import HelloWorld from './components/HelloWorld.vue'
import {ref} from 'vue'
let msg = ref("父传子的元素")
</script>




<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
