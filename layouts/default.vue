<template>
  <v-app>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list dense>
        <v-list-tile
          v-for="link in links"
          :key="link.title"
          :to="link.url"
          exact
          nuxt
          @click="onNavLinkClick">
          <v-list-tile-action>
            <v-icon>{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{ link.title }}</v-list-tile-title>
          </v-list-tile-content>
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
      links: [
        { title: 'Home', icon: 'home', url: '/' },
        { title: 'Contact', icon: 'contact_mail', url: '/contact' },
        { title: 'Blog', icon: 'book', url: '/blog' },
      ],
    }
  },
  computed: {
    year() {
      return new Date().getFullYear()
    },
  },
  methods: {
    onNavLinkClick() {
      if (!this.$vuetify.breakpoint.mdAndUp) {
        this.drawer = false
      }
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
