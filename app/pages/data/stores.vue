<script setup lang='ts'>
const themeStore = useThemeStore()
const dataStore = useDataStore()
const counterStore = useCounterStore()

onMounted(async () => {
  await dataStore.initData()
})
</script>

<template lang="pug">
div.card
  h2 Store Settings
  h5.font-bold.text-2xl.mb-4 Primevue Theme Store
  div.grid.grid-cols-2.gap-4
    div Theme Name
    div {{ themeStore.themeName }}
    div Theme Color
    div {{ themeStore.themeColor }}
  h5.font-bold.text-2xl.mb-4 Data Store (Option Store)
  span.text-xs Example of a Data Store
  div.grid.grid-cols-2.mt-6.gap-4
    div Products
    div {{ dataStore.products.length }}
  h5.font-bold.text-2xl.mb-4 Counter Store (Setup Store)
  span.text-xs Example of a Data Store
  div.mt-6
    div
      InputText(v-model="counterStore.name")
  div.mt-3 {{ counterStore.name }}
    | clicked
    | {{ counterStore.count }}
    | times. Doubled value:
    | {{ counterStore.doubleCount }}
  div.mt-3
    Button(:label="counterStore.name", @click="counterStore.increment()")
</template>

<style lang='scss' scoped>
h5 {
  color: var(--primary-color)
}
</style>
