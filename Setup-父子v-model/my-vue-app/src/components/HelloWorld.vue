
<template>
  <h1>{{ msg }}</h1>
  <button @click="btn">修改父元素</button>
</template>

<script setup>
import { ref ,defineProps,defineEmits} from 'vue'

defineProps({
  msg: String,
})
//子传父
// 使用defineEmits创建名称，接受一个数组
const emit = defineEmits(['update:msg'])

let data = ref("子数据")
//定义要给父亲传递的数据
const btn =()=>{
  //传递给父组件
  emit('update:msg',data.value)
}
const count = ref(0)
</script>
