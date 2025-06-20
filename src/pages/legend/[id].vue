<script setup lang="ts">
import { useFetch, useRoute } from 'nuxt/app'
const route = useRoute()

const { data, pending } = await useFetch('/api/legend', {
  query: { id: route.params.id },
})
</script>

<template>
  <SectionLegend v-if="!pending" :legend-info="data" />
</template>
