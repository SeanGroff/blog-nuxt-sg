<template>
  <footer class="footer">
    <div class="footer--content">
      <base-logo />
      <p class="footer--copyright">
        Copyright © {{ year }}
        <nuxt-link
          class="footer--link"
          to="/">
          sean groff
        </nuxt-link>
      </p>
      <base-icons />
    </div>
  </footer>
</template>

<script>
import BaseLogo from '@/components/BaseLogo'
import BaseIcons from '@/components/BaseIcons'
import { currentYear } from '@/utils'

export default {
  name: 'BaseFooter',
  components: {
    BaseLogo,
    BaseIcons,
  },
  computed: {
    year() {
      return currentYear()
    },
  },
}
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--bgColorDark);
  color: var(--lightText);
  padding: var(--sectionPadding);
  content: '';
  z-index: 5;
}

.footer--content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.footer--copyright {
  font-size: 14px;
  font-family: Lora-Regular;
  line-height: 30px;
  margin: 24px 0;
}

.footer--link {
  color: var(--lighterBlueText);
  font-size: 14px;
  font-family: Lora-Regular;
  line-height: 30px;
  text-decoration: none;
  text-transform: capitalize;
  transition: color 0.2s linear;
}

.footer--link:hover {
  cursor: pointer;
  color: var(--hoverText);
  transition: color 0.2s linear;
}
</style>
