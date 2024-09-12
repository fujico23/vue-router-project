<script setup>
import { ref } from 'vue'
const count = ref(0)
function countUp(event, times) {
  count.value = event.clientX * times
}
</script>

<template>
  <div>
    <p>{{ count }}</p>
    <button @click="count++">button</button> //インラインハンドラ
    <button @click="countUp($event, 5)">button</button> //メソッドハンドラ
  </div>
</template>
