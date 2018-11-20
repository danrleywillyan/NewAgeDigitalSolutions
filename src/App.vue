<template>
<v-app>
  <v-toolbar
    dark
    :clipped-left="clipped"
    app
  >
    <v-toolbar-title>
      <router-link to="/" tag="span" style="cursor: pointer">
        Nova Era Solu&ccedil;&otilde;es Digitais
      </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <span class="hidden-sm-and-up">
      <v-toolbar-side-icon @click="sidebar = !sidebar">
      </v-toolbar-side-icon>
    </span>
    <v-toolbar-items class="hidden-xs-only">
    <v-btn
      flat
      v-for="routes in links"
      :key="routes.text"
      :to="routes.page">
      <v-icon left dark>{{ routes.icon }}</v-icon>
      {{ routes.text }}
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn icon>
      <v-icon>favorite</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>search</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>more_vert</v-icon>
    </v-btn>
  </v-toolbar-items>
  </v-toolbar>
  <v-content>
    <h1>Nova Era Solu&ccedil;&otilde;es Digitais</h1>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-content>
  <Footer></Footer>
</v-app>
</template>

<script>
import Navigation from './components/Navigation'
import Footer from './components/Footer'
export default {
  name: 'App',
  components: {
    'Navigation': Navigation,
    'Footer': Footer
  },
  data () {
    return {
      sidebar: false,
      clipped: false,
      links: [
        {
          text: 'Hello World',
          page: '/',
          icon: 'home'
        },
        {
          text: 'About',
          page: './About',
          icon: 'face'
        },
        {
          text: 'Contact',
          page: './Contact',
          icon: 'lock_open'
        }
      ]
    }
  },
  computed: {
    platform () {
      return '$vuetify.icons.' + this.user.platform
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
