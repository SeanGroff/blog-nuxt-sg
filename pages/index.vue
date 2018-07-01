<template>
  <div class="wrapper">
    <base-me />
    <base-about-preview />
    <base-portfolio-preview />
    <base-contact-preview />
    <base-footer />
  </div>
</template>

<script>
import BaseMe from '@/components/BaseMe'
import BaseAboutPreview from '@/components/BaseAboutPreview'
import BasePortfolioPreview from '@/components/BasePortfolioPreview'
import BaseContactPreview from '@/components/BaseContactPreview'
import BaseFooter from '@/components/BaseFooter'

export default {
  name: 'IndexPage',
  components: {
    BaseMe,
    BaseAboutPreview,
    BasePortfolioPreview,
    BaseContactPreview,
    BaseFooter,
  },
}
</script>

<style lang="postcss" scoped>
.wrapper {
  height: 100%;
  width: 100%;
}
</style>
