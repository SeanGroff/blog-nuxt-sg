<template>
  <div class="navBar">
    <div class="leftColumn">
      <base-logo />
    </div>
    <div class="rightColumn">
      <base-link nav-route="blog">blog</base-link>
      <base-link nav-route="about">about</base-link>
      <base-link nav-route="portfolio">portfolio</base-link>
      <base-link nav-route="contact">contact</base-link>
      <base-hamburger-menu @toggleMenu="open = !open" />
    </div>
  </div>
</template>

<script>
import BaseHamburgerMenu from '@/components/BaseHamburgerMenu'
import BaseLogo from '@/components/BaseLogo'
import BaseLink from '@/components/BaseLink'
export default {
  name: 'NavBar',
  components: {
    BaseHamburgerMenu,
    BaseLogo,
    BaseLink,
  },
  data() {
    return {
      open: false,
    }
  },
}
</script>

<style lang="postcss" scoped>
.navBar {
  display: flex;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  background-color: var(--bgColorDark);
  height: 50px;
  padding: 0 20px;
  color: var(--lightText);
  box-shadow: 0 1px 3px 0 rgba(20, 20, 20, 0.8);
  content: '';
  z-index: 5;
}

@media (min-width: 992px) {
  .navBar {
    box-shadow: none;
    background-color: transparent;
  }
}

.leftColumn {
  display: flex;
  align-items: center;
  flex: 1 1 auto;
  padding: 0 15px;
}

.rightColumn {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex: 1 1 auto;
  position: relative;
}
</style>
