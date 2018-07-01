<template>
  <div class="default-layout">
    <nav-bar />
    <nuxt />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar'
import { currentYear } from '../utils'

export default {
  name: 'Layout',
  components: {
    NavBar,
  },
}
</script>

<style lang="postcss" scoped>
.default-layout {
  height: 100vh;
  position: relative;
}
</style>
