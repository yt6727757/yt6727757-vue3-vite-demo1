<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1 @click="say">{{msg}}</h1>
</template>

<script>

export default {
  name: 'App',
  // 1、setup 组合api的起点，将来组合api的代码，基本上在这里。
  // 2、可以理解为：在beforeCreate钩子执行之前执行。组件实例创建前
  // 3、函数中不能使用this
  // 4、模板中使用的数据和函数，必须在setup中返回
  setup () {
    console.log(this)
    const msg = 'hi vue3'
    const say = () => {
      console.log(msg)
    }
    return { msg, say }
  },
  beforeCreate () {
    console.log('beforeCreate')
  }
}
</script>
