<script setup lang='ts'>
const collapsed = useState<boolean>('collapsed')
const isOnMobile = useState<boolean>('isOnMobile')
</script>

<template lang="pug">
div
  ConfirmDialog
  Toast
  AppSidebar
  div#workspace(:class="[{ collapsed }, { mobile: isOnMobile }]")
    AppTopbar
    div.m-1.mt-4
      slot
</template>

<style lang="scss">

</style>
