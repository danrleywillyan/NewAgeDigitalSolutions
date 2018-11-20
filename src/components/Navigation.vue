<template>
  <div>
    <v-navigation-drawer
    persistent
    :mini-variant="miniVariant"
    :clipped="clipped"
    v-model="drawer"
    enable-resize-watcher
    fixed
    app
  >
  <v-list>
    <v-list-tile
      v-for="routes in links"
      :key="routes.text"
      :to="routes.page"
    >
    <v-list-tile-action>
      <v-icon>{{routes.icon}}</v-icon>
    </v-list-tile-action>
    <v-list-tile-content>
      {{routes.text}}
    </v-list-tile-content>
    </v-list-tile>
  </v-list>
  </v-navigation-drawer>
    <v-toolbar-items class="hidden-xs-only">
    <v-btn
      flat
      v-for="routes in links"
      :key="routes.text"
      :to="routes.page">
      <v-icon left dark>{{ routes.icon }}</v-icon>
      {{ routes.text }}
    </v-btn>
  </v-toolbar-items>
</div>
</template>

<script>
export default {
  name: 'Navigation',
  data () {
    return {
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

<style scoped>
  * {
    display: inline;
  }
</style>
