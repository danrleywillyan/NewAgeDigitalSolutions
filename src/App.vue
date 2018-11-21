<template>
<v-app :style="cssTheme" class="app-style">
  <v-toolbar
    color="secondary darken-2"
    dark
    :clipped-left="clipped"
    fixed
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
          text: 'Team',
          page: './Team',
          icon: 'group'
        },
        {
          text: 'Contact',
          page: './Contact',
          icon: '$vuetify.icons.contact'
        }
      ]
    }
  },
  computed: {
    platform () {
      return '$vuetify.icons.' + this.user.platform
    },
    cssTheme () {
      const out = {}
      for (const name of Object.keys(this.$vuetify.theme)) {
        out[`--v-color-${name}`] = this.$vuetify.theme[name]
      }
      out['--v-primary-text-color'] = 'rgba(0,0,0,.87)'
      out['--v-secondary-text-color'] = 'rgba(0,0,0,.54)'
      return out
    }
  }
}
</script>

<style scoped lang="css">
.app-style {
  background: #FFFFFF;
  background: -webkit-linear-gradient(to right, #1B5E20, #2ac92f, #1B5E20);
  background: linear-gradient(to right, #1B5E20, #2ac92f, #1B5E20);
}

/*below isnt my own style*/
.vv-logo {
  max-width: 100%;
}

.vv-heading {
  padding-bottom: 30px;
}

.vv-cta {
  padding-top: 30px;
}

.vv-patreon-logo {
  max-width: 22px;
  margin-right: 5px;
}

.vv-card-text {
  padding-top: 15px;
}

@media (max-width: 960px) {
  .vv-heading {
    padding-bottom: 15px;
  }

  .vv-logo {
    max-width: 240px;
  }

  .vv-cta {
    padding-top: 10px;
    text-align: center;
  }
}

@media (max-width: 420px) {
  .vv-heading {
    padding-bottom: 10px;
    line-height: 100%;
  }

  .vv-logo {
    max-width: 160px;
  }

  .vv-cta {
    padding-top: 10px;
    text-align: center;
  }
}
</style>
