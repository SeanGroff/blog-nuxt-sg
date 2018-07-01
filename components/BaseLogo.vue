<template>
  <nuxt-link
    class="logo"
    to="/">
    SG
  </nuxt-link>
</template>

<style lang="postcss" scoped>
.logo {
  color: var(--lightText);
  font-size: 18px;
  font-family: OpenSans-Regular;
  letter-spacing: 2px;
  text-transform: uppercase;
  text-decoration: none;
  transition: color 0.2s linear;
}

.logo:hover {
  cursor: pointer;
  color: var(--hoverText);
  transition: color 0.2s linear;
}
</style>
