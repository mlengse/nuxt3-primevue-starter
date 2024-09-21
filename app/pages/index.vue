<script setup lang='ts'>
import AdvertiseBox from '@/components/AdvertiseBox.vue'
</script>

<template lang="pug">
.card.surface-0.text-center
  .mb-3.font-bold.text-4xl
    span.text-green-600 PrimeVue
    span.text-blue-400  & TypeScript
    span.text-green-400  & Nuxt 3
  h2.text-2xl.pb-6 Starter for Vue.js Development with Nuxt 3.
  .grid.grid-cols-2.gap-2(class="lg:grid-cols-3")
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="PrimeVue 4.x"
      )
      | Excellent
      ExternalLink(
        text="Component Library" 
        href="https://github.com/sfxcode/formkit-primevue"
        ) for VUE
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="PrimeVue Theme"
      )
      ExternalLink(
        text="Styled Mode" 
        href="https://primevue.org/theming/styled"
        ) with preset: Aura
    AdvertiseBox(
      color="purple-500" 
      icon="prime-check-circle" 
      header="FormKit"
      )
      ExternalLink(
        text="Formkit" 
        href="https://formkit.com"
        )
        | 1.6.x support by
        ExternalLink(
          text="PrimeVue-FormKit" 
          href="https://formkit-primevue.netlify.app/"
          )
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="UnoCSS"
      )
      ExternalLink(
        text="UnoCSS" 
        href="https://unocss.dev/"
        ) for rapid styling
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="VUE 3.5.x"
      )
      ExternalLink(
        text="Composition Api" 
        href="https://vuejs.org/guide/introduction.html"
        ) with Script Setup
    AdvertiseBox(
      color="blue-400" 
      icon="prime-check-circle" 
      header="Typescript 5"
      ) Typesafe by default
    AdvertiseBox(
      color="green-400" 
      icon="prime-check-circle" 
      header="Nuxt 3.13.x (Nuxt 4 ready)"
      )
      ExternalLink(
        text="Nuxt" 
        href="https://nuxt.com/"
        ) with Pages, Layouts, ...
    AdvertiseBox(
      color="green-400" 
      icon="prime-check-circle" 
      header="Nuxt Content 2.13.x"
      )
      ExternalLink(
        text="Content" 
        href="https://content.nuxt.com/"
        ) : Markdown, YML, CSV or JSON and MDC Syntax
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="Nuxt Modules"
      )
      | includes
      ExternalLink(
        text="Nuxt Images" 
        href="https://nuxt.com/modules/image"
        )
        | ,
        ExternalLink(
          text="Nuxt Fonts" 
          href="https://nuxt.com/modules/fonts"
          )
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="VueUse"
      )
      ExternalLink(
        text="VueUse" 
        href="https://vueuse.org/"
        ) included
    AdvertiseBox(
      color="blue-400" 
      icon="prime-check-circle" 
      header="Pinia 2.x"
      )
      ExternalLink(
        text="Pinia" 
        href="https://pinia.vuejs.org/"
        ) : Vue Store Implementation
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="TipTap"
      )
      ExternalLink(
        text="TipTap" 
        href="https://tiptap.dev/"
        ) Editor
    AdvertiseBox(
      color="green-600" 
      icon="prime-check-circle" 
      header="Vue Sidebar"
      )
      ExternalLink(
        text="Sidebar" 
        href="https://github.com/yaminncco/vue-sidebar-menu"
        ) component
    AdvertiseBox(
      color="green-400" 
      icon="prime-check-circle" 
      header="Nitro"
      )
      ExternalLink(
        text="Nitro" 
        href="https://nitro.unjs.io/"
        ) : Next Generation Server Toolkit
    AdvertiseBox(
      color="blue-600" 
      icon="prime-check-circle" 
      header="Vitest"
      ) Testing with Vitest
</template>

<style scoped></style>
