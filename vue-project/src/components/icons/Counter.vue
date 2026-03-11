<script setup>
import { ref } from 'vue'

// reactive state
const count = ref(0)

// trigger reactivity
function increment() {
  count.value++
} 
</script>

<template>
  <div>
    <button @click="increment">Click Me {{ count }}</button>
  </div>
</template>