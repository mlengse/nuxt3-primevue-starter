<script setup lang='ts'>
const { d, t, n, locale, locales, setLocale } = useI18n()
const testDate = new Date()
const testNumber = 42.4242

const availableLocales = computed(() => {
  return locales.value?.filter(l => l.code !== locale.value)
})
</script>

<template lang="pug">
div.card
  h2 Localization
  | Switch Locale to 
  a(v-for="currentLocale in availableLocales", :key="currentLocale.code", href="#", @click.prevent.stop="setLocale(currentLocale.code)")  {{ currentLocale.name }}
  p {{ t(&apos;save&apos;) }}
  p {{ d(testDate, &apos;short&apos;) }}
  p {{ n(testNumber, &apos;currency&apos;) }}

</template>

<style scoped></style>
