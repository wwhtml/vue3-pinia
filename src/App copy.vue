<script lang="ts" setup>
import { useCounterStore } from '@/stores/counter'

import { storeToRefs } from 'pinia'

const counter = useCounterStore()

const { count, doubelCount } = storeToRefs(counter)

const increase = () => {
  count.value++
}
</script>

<template>
  <div>
    <button @click="increase">increase</button>

    <p>{{ count }}</p>
    <p>{{ doubelCount }}</p>
  </div>
</template>

<style scoped lang="scss"></style>
