<script setup lang='ts'>
const route = useRoute()
const slug = route.params.slug?.toString()
</script>

<template lang="pug">
div.markdown
  ContentDoc(:path="slug")
    template(#default="{ doc }")
      div.card
        h2 {{ doc.title }}
        p {{ doc.description }}
        p.font-bold Author:
          | {{ doc.author }}
        hr
        ContentRenderer(:value="doc")
    template(#not-found)
      h1.text-2xl Content Page (
        | {{ slug }}
        | ) not found
</template>

<style scoped></style>
