<template>
  <div>
    <h1>{{test}}</h1>
    <p>{{obj}}</p>
    <button @click="btn">修改按钮</button>
    //引入HelloWorld模块并传递msg参数
<!--    <HelloWorld msg="Vite + Vue" />-->
    <hr />
<!--计算属性-->
    {{c}}
<!--监听属性-->
    <input type="" name="" v-model='wh'>
    <h1>{{wh}}</h1>
  </div>
</template>


<script setup>
import {ref,reactive,computed,watch} from 'vue'
//必须导入，不然不生效
import HelloWorld from './components/HelloWorld.vue'
//定义字符串
let test = ref("测试fjdsklfjldskjfldsjflkdsj")
//定义对象
let obj = reactive({
  a:1,
  b:2
})
//自定义函数
const btn = ()=>{
  console.log(test.value)
  test.value = "test"
  obj.b= "测试"
}
//计算属性:二次计算后端传来的数据，并进行修改
// 例如：截取1-5
// 结果：试fjd
let c = computed(()=>{
  return test.value.slice(1,5)
})
//监听属性
let wh = ref("1234567")
let sw = watch(wh,(newVal,oldVal)=>{
  test.value="监听数据"
  console.log(newVal,oldVal)
})
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
