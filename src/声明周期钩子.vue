<template>
  <div class="container">
    组件
  </div>
</template>

<script>
import { onBeforeMount, onMounted } from 'vue'
export default {
  name: 'App',
  setup () {
    onBeforeMount(() => {
      console.log('onBeforeMount', document.querySelector('.container'));
    })

    onMounted(() => {
      console.log('onMounted1', document.querySelector('.container'));
    })

    onMounted(() => {
      console.log('onMounted2', document.querySelector('.container'));
    })
  }
}
</script>
