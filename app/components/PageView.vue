<script setup lang="ts">
const { data } = await useFetch('/api/pageview')
const time = useTimeAgo(Number(computed(() => data.value?.startAt)))
const pageview = data.value?.pageview
</script>

<template lang="pug">
.text-2xl(class='text-gray:80')
  span(font-500 text-gray) {{ pageview }} page views since
  span(text-gray) {{ time }}
</template>
