<template>
  <button @click="button">子组件</button>
</template><script setup>


import { ref,defineProps } from 'vue'

defineProps({
  msg: String,
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
const count = ref(0)
</script>

