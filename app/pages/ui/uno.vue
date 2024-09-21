<script setup lang='ts' xmlns:all="http://www.w3.org/1999/xhtml">
const config = useRuntimeConfig()
</script>

<template lang="pug">
.card
  h2 UnoCSS
  div(h-full text-center flex select-none all:transition-400)
    div(ma)
      div(text-6xl font-bold fw100 animate-bounce-alt animate-count-infinite animate-5s)
        | unocss
      div(dark:op30 text-lg fw300 m1)
        | The instant on-demand Atomic CSS engine.
      div(m2 flex justify-center text-2xl dark:op30 hover='op80')
        a(i-mdi-github-circle text-inherit text-8xl href='https://github.com/antfu/unocss' target='_blank')
  div(bottom-5 right-0 left-0 text-center dark:op30 fw300)
    | on-demand &middot; instant &middot; fully customizable
  client-only
    div(v-if="'development' === config.public.APP_MODE")
      h4(pt-30)
        | Inspector
      div(pb-4)
        span Only visible in Development mode - click info icon below
      a(href='../__unocss' target='_blank')
        .i-mdi-information.text-4xl.text-green-600-500-500
      article.pt-4.text-base.prose.prose-truegray(class='xl:text-xl')
        | View, play and analyse rules and setup ...

</template>

<style scoped></style>
