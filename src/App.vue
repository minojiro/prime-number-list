<script setup lang="ts">
import { computed } from 'vue'

const MAX_NUMBER = 10_000

const primeNumbers = computed(() => {
  const s = new Set<number>()
  const l: number[] = []
  for (let n = 2; n <= MAX_NUMBER; n++) {
    if (s.has(n)) continue
    for(let n2 = n; n2 <= MAX_NUMBER; n2 += n) {
      s.add(n2)
    }
    l.push(n)
  }
  return l
})
</script>

<template>
  <main>
    <h1>素数</h1>
    <ul>
      <li v-for="number in primeNumbers">{{ number }}</li>
    </ul>
    <hr>
    <p><a href="https://github.com/minojiro/prime-number-list" rel="noopener" target="_blank">repository</a></p>
  </main>
</template>
