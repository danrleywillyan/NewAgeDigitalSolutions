<template>
  <v-footer
    dark
    height="auto"
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">
        <strong class="subheading">
          Crie uma conex&atilde;o com sua solu&ccedil;&atilde;o digital atrav&eacute;s
          das redes sociais.
        </strong>
        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-3"
          dark
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-title>

      <v-card-actions class="grey darken-3 justify-center">
        &copy;2018 — <strong>Grupo de M&iacute;dias e Comunica&ccedil;&otilde;es Digitais</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    icons: [
      'fab fa-facebook',
      'fab fa-github',
      'fab fa-youtube',
      'fab fa-linkedin',
      'fab fa-instagram'
    ]
  })
}
</script>
