<script lang="ts" setup>
import { useCounterStore } from '@/stores/counter'

const counter = useCounterStore()

const increase = () => {
  counter.count++
}

const reset = () => {
  counter.$reset() //无效
}
</script>

<template>
  <div>
    <button @click="increase">increase</button>
    <button @click="reset">reset</button>

    <p>{{ counter.count }}</p>
    <p>{{ counter.doubleCount }}</p>
  </div>
</template>

<style scoped lang="scss"></style>
