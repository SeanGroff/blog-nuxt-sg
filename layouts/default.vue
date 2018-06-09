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
          @click="close">
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
    close() {
      if (!this.$vuetify.breakpoint.mdAndUp) {
        this.drawer = false
      }
    },
  },
}
</script>

<style>
a {
  text-decoration: none;
}

.article--preview {
  margin-bottom: 32px !important;
}

.article--title {
  font-size: 24px;
  font-weight: 600;
}

.article--meta {
  margin-bottom: 8px;
}

.article--description {
  color: #2c3e50;
  font-size: 16px;
}

.blog-article-container .blog-article {
  color: #2c3e50;
  font-size: 16px;
  max-width: 280px;
  margin: 0 auto;
}

@media (min-width: 640px) {
  .blog-article-container .blog-article {
    max-width: 740px;
  }
}

.blog-article-container .blog-article-title {
  color: rgb(44, 62, 80);
  margin-top: -24px;
  margin-bottom: 16px;
  padding-top: 74px;
  font-size: 36px;
  font-weight: 600;
  line-height: 1.25;
}

.blog-article-container .blog-article-meta {
  margin-bottom: 8px;
}

.blog-article-container .blog-article-content p img {
  display: block;
  max-width: 280px;
  margin: 0 auto;
}

@media (min-width: 640px) {
  .blog-article-container .blog-article-content p img {
    max-width: 640px;
  }
}

.blog-article-container .blog-article-content h2 {
  display: block;
  color: rgb(44, 62, 80);
  font-size: 26px;
  font-weight: 600;
  padding: 24px 0;
}
</style>
