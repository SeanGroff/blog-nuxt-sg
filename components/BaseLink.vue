<template>
  <nuxt-link
    :to="`/${navRoute}`"
    class="link">
    <slot />
  </nuxt-link>
</template>

<script>
export default {
  props: {
    navRoute: {
      type: String,
      default: 'home',
      required: true,
    },
  },
}
</script>

<style scoped>
.link {
  display: none;
}

@media (min-width: 992px) {
  .link {
    display: inline-block;
    color: var(--lightText);
    font-family: OpenSans-Light;
    font-size: 13px;
    padding: 0 13px;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    transition: color 0.2s linear;
  }

  .link:hover {
    cursor: pointer;
    color: var(--hoverText);
    transition: color 0.2s linear;
  }
}
</style>
