<template>
  <div class="contact-preview">
    <base-heading :is-light-text="false">contact me</base-heading>
    <a
      ref="noopener"
      href="mailto:sgroff04@gmail.com"
      class="mail">
      Email Me
    </a>
  </div>
</template>

<script>
import BaseHeading from '@/components/BaseHeading'

export default {
  name: 'BaseContactPreview',
  components: {
    BaseHeading,
  },
}
</script>

<style lang="postcss" scoped>
.contact-preview {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--bgColorLight);
  padding: var(--sectionPadding);
}

.mail {
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--ctaText);
  font-size: 14px;
  font-family: Lora-Regular;
  line-height: 30px;
  text-decoration: none;
  background-color: var(--bgColorLight);
  border: 2px solid var(--ctaText);
  border-radius: 5px;
  padding: 5px 10px;
  width: 100px;
  transition: all 0.2s ease-in-out;
}

@media (min-width: 992px) {
  .mail:hover {
    background-color: var(--ctaText);
    color: var(--lightText);
    cursor: pointer;
    transition: all 0.2s ease-in-out;
  }
}
</style>
