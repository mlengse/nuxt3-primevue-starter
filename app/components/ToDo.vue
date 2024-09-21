<script setup lang='ts'>
defineProps({
  text: {
    type: String,
    default: 'TODO',
  },
})
</script>

<template lang="pug">
div
  .todo.m-4.flex.gap-2
    i.i-mdi-information.text-3xl(class='text-[color:var(--primary-color)]')
      .text-2xl(data-testid='test_todo') {{ text }}
  .pt-4.pl-1
    slot
</template>

<style scoped>

</style>
