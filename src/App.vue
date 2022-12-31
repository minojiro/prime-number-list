<script setup lang="ts">
import { computed } from 'vue'
const primeNumbers = computed(() => {
  return [
    2, 3, 5, 7, 11
  ]
})
</script>

<template>
  <main>
    <h1>素数</h1>
    <ul>
      <li v-for="number in primeNumbers">{{ number }}</li>
    </ul>
  </main>
</template>
