<script setup>
  import { ref } from 'vue'
  const count = ref(0)

  function increment() {
    count.value++
  }

  function decrement() {
    count.value--
  }
</script>

<template>
  <div>
    counter:
    <input type="text" disabled :value="count">
    <button @click="decrement">-</button>
    <button @click="increment">+</button>
  </div>
</template>

<style>
div {
  color: white;
}
</style>