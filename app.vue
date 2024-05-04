<script lang="ts" setup>
import { useCounterStore } from '@/store/counter'


const counterStore = useCounterStore()


function increment() {
  counterStore.increment()
}


function reset() {
  counterStore.$reset()
}
</script>

<template>
  <div>
    <div>
      <button @click="increment()">increment</button>
      <button @click="reset()">reset</button>
    </div>
    <div>count: {{ counterStore.count }}</div>
    <div>double: {{ counterStore.double }}</div>
  </div>
</template>
