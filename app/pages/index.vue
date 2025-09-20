<script lang="ts" setup>
import { ref } from 'vue'
import { legendsMock } from '../mock/index.ts'

const legends = ref([...legendsMock])
</script>
<template>
  <AppHero />
  <SectionCtaLegends :legends="legends" />
</template>
