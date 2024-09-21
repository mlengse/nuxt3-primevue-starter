<script setup lang='ts'>
import ToDo from '~/components/ToDo.vue'
</script>

<template lang="pug">
div.card
  h2 Blueprint
  p Use this page to start from scratch and place your custom content !
  NuxtLink(to="/") Home page
  div
    ToDo(text="Work in Progress")
</template>

<style scoped></style>
