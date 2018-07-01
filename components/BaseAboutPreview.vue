<template>
  <section class="about">
    <base-heading :is-light-text="false">about me</base-heading>
    <p class="content">
      I am a Full-Stack Web Developer with a focus on front-end development. I am well versed with VueJS, React, Redux, HTML, CSS, GraphQL, Apollo, Node, Express, and MongoDB. Learning new things and staying on the bleeding edge of JavaScript is my passion. I strive for pixel perfect responsive styles, code reuse and code maintainability.
    </p>
  </section>
</template>

<script>
import BaseHeading from '@/components/BaseHeading'

export default {
  name: 'BaseAboutPreview',
  components: {
    BaseHeading,
  },
}
</script>

<style lang="postcss" scoped>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--bgColorLight);
  padding: var(--sectionPadding);
}

.content {
  font-size: 16px;
  font-family: Lora-Regular;
  line-height: 30px;
  color: var(--darkText);
  margin: 0;
  max-width: 968px;
  padding: 0 10px;
}
</style>
