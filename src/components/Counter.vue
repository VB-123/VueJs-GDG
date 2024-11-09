<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
}

const decrement = () => {
  count.value--
}

const reset = () => {
  count.value = 0
}
</script>

<template>
  <div class="counter">
    <h2>Counter: {{ count }}</h2>
    <div class="buttons">
      <button @click="decrement"> - </button>
      <button @click="increment"> + </button>
      <button @click="reset"> Reset </button>
    </div>
  </div>
</template>

<style scoped>
h2{
  background-color:#f0f0f0;
  color: #000000;
}
.counter {
  text-align: center;
  padding: 20px;
}

.buttons {
  display: flex;
  gap: 10px;
  justify-content: center;
  margin-top: 10px;
}

button {
  padding: 8px 16px;
  font-size: 16px;
  cursor: pointer;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #f0f0f0;
}

button:hover {
  background-color: #e0e0e0;
}
</style>
