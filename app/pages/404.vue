<script setup lang="ts">
const router = useRouter()
</script>

<template lang="pug">
.card
  .col-12.mt-10.text-center
    img.mb-5(
      style="width:81px; height:60px;" 
      alt="Nuxt logo" 
      src="/nuxt-logo.svg"
      )
  main.px-4.py-10.text-center.text-teal-700.text-8xl
    div
      p.text-8xl.text-red-600
        span.i-codicon-error.inline-block
  div(style="alignment: center")
    h1.font-bold.text-5xl.text-2xl.text-center Page not found ...
    .col-12.mt-5.text-center
      button(
        data-tag="Button" 
        @click="router.push('/')" 
        label="Back to home" 
        icon="pi pi-arrow-left"
        )
</template>
