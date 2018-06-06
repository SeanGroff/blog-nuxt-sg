<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list dense>
        <v-list-tile @click="drawer = false">
          <nuxt-link
            to="/"
            exact>
            <v-list-tile-action>
              <v-icon>home</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Home</v-list-tile-title>
            </v-list-tile-content>
          </nuxt-link>
        </v-list-tile>

        <v-list-tile @click="drawer = false">
          <nuxt-link
            to="/contact"
            exact>
            <v-list-tile-action>
              <v-icon>contact_mail</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Contact</v-list-tile-title>
            </v-list-tile-content>
          </nuxt-link>
        </v-list-tile>

        <v-list-tile @click="drawer = false">
          <nuxt-link
            to="/blog"
            exact>
            <v-list-tile-action>
              <v-icon>book</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Blog</v-list-tile-title>
            </v-list-tile-content>
          </nuxt-link>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      color="primary"
      dark
      fixed
      app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"/>
      <v-toolbar-title>SG</v-toolbar-title>
    </v-toolbar>
    <v-content>
      <v-container
        fluid
        fill-height>
        <v-layout
          justify-center
          align-center>
          <nuxt />
        </v-layout>
      </v-container>
    </v-content>
    <v-footer
      color="primary"
      app
      dark>
      <span class="white--text">{{ `&copy; ${year}` }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'Layout',
  data() {
    return {
      drawer: null,
    }
  },
  computed: {
    year() {
      return new Date().getFullYear()
    },
  },
}
</script>

<style scoped>
a {
  display: flex;
  flex: 1 1 auto;
  text-decoration: none;
}
</style>
