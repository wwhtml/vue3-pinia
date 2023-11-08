<script lang="ts" setup>
import { useCounterStore } from '@/stores/counter'

const counter = useCounterStore()

const increase = () => {
  counter.count++
}
</script>

<template>
  <div>
    <button @click="increase">increase</button>

    <p>{{ counter.count }}</p>
    <p>{{ counter.doubelCount }}</p>
  </div>
</template>

<style scoped lang="scss"></style>
