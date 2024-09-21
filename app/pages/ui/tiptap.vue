<script setup lang="ts">
import TipTap from '~/components/tiptap/TipTap.vue'

const startText = '<p>I’m running <strong>Tiptap</strong> with <strong>Vue.js</strong> and <strong>Nuxt</strong>. 🎉</p><hr><blockquote><p>Use TipTap ...</p></blockquote>\n'
const editorValue = ref(startText)

function resetText() {
  editorValue.value = startText
}
</script>

<template lang="pug">
.card
  h2 TipTap as alternative Editor
  .pb-2
    Button(
      data-tag="Button" 
      @click="resetText" 
      label="Reset" 
      size="small"
      )
  .p-tiptap
    TipTap(v-model="editorValue")
  .pt-8
    pre(v-if="false") {{ editorValue }}</template>

<style lang='scss'>

</style>
