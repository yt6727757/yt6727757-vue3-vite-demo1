<template>
  <div class="container">
    <div>{{obj.name}}</div>
    <div>{{obj.age}}</div>
    <button @click="updateName">修改名字</button>
    <br>
    <input type="text" v-model="obj.name">
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup () {
    //  reactive 通常用来定义响应式对象
    const obj = reactive({
      name: 'zs',
      age: 22
    })
    const updateName = () => {
      obj.name = '张三'
      console.log(obj)
    }
    return { obj, updateName }
  }
}
</script>

