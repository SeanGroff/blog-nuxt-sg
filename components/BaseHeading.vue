<template>
  <h1
    :class="{ whiteText: isLightText, blueText: !isLightText }"
    class="heading">
    <slot />
  </h1>
</template>

<script>
export default {
  props: {
    isLightText: {
      type: Boolean,
      default: true,
      required: true,
    },
  },
}
</script>

<style lang="postcss" scoped>
.whiteText {
  color: var(--lightText);
}

.blueText {
  color: var(--lightBlueText);
}

.heading {
  font-size: 28px;
  font-family: OpenSans-Bold;
  text-align: center;
  text-transform: uppercase;
  margin: 0 0 20px 0;
}

@media (min-width: var(--mediumUp)) {
  .heading {
    font-size: 48px;
  }
}
</style>
