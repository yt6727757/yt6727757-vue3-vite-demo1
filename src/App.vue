<template>
  <div>
    <div>{{obj.name}}</div>
    <button @click="updateName">修改</button>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  name: 'App',
  setup () {
    const obj = reactive({
      name: '张三',
      age: 22
    })
    const updateName = () => {
      obj.name = '李四'
    }
    return { obj, updateName }
  },
}
</script>

<style scoped lang='less'>
</style>
