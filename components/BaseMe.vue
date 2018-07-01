<template>
  <header class="hero">
    <div class="me">
      <div class="avatar" />
      <h1 class="name">sean groff</h1>
      <h2 class="occupation">web developer</h2>
      <base-icons />
    </div>
  </header>
</template>

<script>
import BaseIcons from '@/components/BaseIcons'

export default {
  name: 'BaseMe',
  components: {
    BaseIcons,
  },
}
</script>


<style scoped>
.hero {
  background: linear-gradient(
      var(--transparentDarkBlue),
      var(--transparentDarkBlue)
    ),
    url('../assets/hero1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}

.me {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 15px;
  margin-top: -50px;
  color: var(--lightText);
}

.avatar {
  border: 3px solid var(--bgColorLight);
  border-radius: 50%;
  background: url('../assets/profilePic.jpg');
  background-size: contain;
  background-repeat: no-repeat;
  width: 150px;
  height: 150px;
}

.name {
  font-size: 40px;
  font-family: OpenSans-Bold;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin: 20px 0;
  padding-bottom: 20px;
  border-bottom: 1px solid var(--lightText);
  border-bottom-color: rgba(236, 240, 241, 0.35);
}

@media (min-width: var(--mediumUp)) {
  .name {
    font-size: 60px;
  }
}

.occupation {
  font-size: 24px;
  font-family: OpenSans-Light;
  text-transform: capitalize;
  margin: 0;
  margin-bottom: 20px;
}

@media (min-width: var(--mediumUp)) {
  .occupation {
    font-size: 30px;
  }
}
</style>
