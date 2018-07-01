<template>
  <div class="icons">
    <a
      href="https://www.github.com/SeanGroff"
      target="_blank"
      class="icon"
      rel="noopener">
      <i
        class="fa fa-github"
        aria-hidden="true" />
    </a>
    <a
      href="https://www.twitter.com/_SeanGroff"
      target="_blank"
      class="icon"
      rel="noopener">
      <i
        class="fa fa-twitter"
        aria-hidden="true" />
    </a>
    <a
      href="https://www.linkedin.com/in/sgroff"
      target="_blank"
      class="icon"
      rel="noopener">
      <i
        class="fa fa-linkedin"
        aria-hidden="true" />
    </a>
    <a
      href="https://www.medium.com/@sgroff04"
      target="_blank"
      class="icon"
      rel="noopener">
      <i
        class="fa fa-medium"
        aria-hidden="true" />
    </a>
    <a
      href="https://codepen.io/sgroff04"
      target="_blank"
      class="icon"
      rel="noopener">
      <i
        class="fa fa-codepen"
        aria-hidden="true" />
    </a>
  </div>
</template>

<style lang="postcss" scoped>
.icons {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.icon {
  color: var(--lightText);
  font-size: 24px;
  padding: 0 8px;
  transition: color 0.2s linear;
}

.icon:hover {
  cursor: pointer;
  color: var(--hoverText);
  transition: color 0.2s linear;
}
</style>
