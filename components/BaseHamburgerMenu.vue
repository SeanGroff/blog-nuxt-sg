<template>
  <div
    class="menu"
    @click="$emit('toggleMenu')">
    <div class="lines" />
  </div>
</template>

<style lang="postcss" scoped>
.menu {
  display: block;
  position: relative;
}

@media (min-width: 992px) {
  .menu {
    display: none;
  }
}

.menu::before {
  position: absolute;
  top: -14px;
  padding: 15px;
  content: '';
  z-index: 10;
}

.menu:hover {
  cursor: pointer;
}

.lines {
  position: relative;
  padding-right: 15px;
  width: 28px;
  border-top: 3px solid var(--lightText);
}

.lines::before {
  position: absolute;
  transform: translateY(-10px);
  content: '';
  width: 28px;
  border-top: 3px solid var(--lightText);
}

.lines::after {
  position: absolute;
  transform: translateY(4px);
  content: '';
  width: 28px;
  border-top: 3px solid var(--lightText);
}
</style>
