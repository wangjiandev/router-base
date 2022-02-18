<script setup>
import { computed } from 'vue'
import router from '../router'
import { path } from '../router'

const view = computed(() => {
  const currentRoute = router.routes.find((route) => route.path === path.value)
  return currentRoute.component
})
</script>

<template>
  <component :is="view"></component>
</template>

<style scoped></style>
