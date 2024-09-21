<script setup lang='ts'>
import { useCounter } from '#imports'

const count = useCounter()
</script>

<template lang="pug">
div.card
  h2 Server API Usage
  PageView
  h2 Counter (useState)
  div.grid.grid-cols-3.w-80.mt-8
    Button(icon="pi pi-plus", @click="count.inc()").p-button-rounded.p-button-info
    span.text-4xl {{ count.count }}
    Button(icon="pi pi-minus", @click="count.dec()").p-button-rounded.p-button-success
</template>

<style scoped></style>
