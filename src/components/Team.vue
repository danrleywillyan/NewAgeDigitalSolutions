<template>
  <v-container fluid grid-list-lg>
    <v-layout wrap justify-center>
      <v-flex d-flex xs12 sm6 md4 lg4>
        <v-card contain>
          <v-img
            class="white--text"
            height="350px"
            src="/static/Israel.jpg"
          >
            <v-container fill-height fluid>
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline">Israel<br> Carvalho</span>
                </v-flex>
              </v-layout>
            </v-container>
          </v-img>
          <v-card-title>
            <div>
              <span class="grey--text">Diretor Executivo</span><br>
              <span>Idealizador do Gama Cidad&atilde;o (Portal de Not&iacute;cias do Gama)</span><br>
              <span><b>"Cidad&atilde;o informado &eacute; cidad&atilde;o consciente."</b></span><br><br>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Facebook
            </v-btn>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Linkedin
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      <v-flex d-flex xs12 sm6 md4 lg4>
        <v-card contain>
          <v-img
            class="dark--text"
            height="350px"
            :src="'/static/danrley.jpeg'"
          >
            <v-container fill-height fluid>
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline">Danrley<br> Pereira</span>
                </v-flex>
              </v-layout>
            </v-container>
          </v-img>
          <v-card-title>
            <div>
              <span class="grey--text">Desenvolvedor de Software</span><br>
              <span>Apaixonado por desenvolvimento web.</span><br>
              <span>
                <b>
                "Site bom &eacute; aquele que disponibiliza a
                melhor experi&ecirc;ncia para o usu&aacute;rio."
                </b>
              </span><br><br>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn href="https://danrleywillyan-blog.firebaseapp.com/" target="_blank"
              depressed small color="accent"
            >
              Blog Pessoal
            </v-btn>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Linkedin
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      <v-flex d-flex xs12 sm6 md4 lg4>
        <v-card contain>
          <v-img
            class="dark--text"
            height="350px"
            aspect-ratio="1.225114854517611"
            v-bind:src="'/static/rodrigo.png'"
          >
            <v-layout slot="placeholder" fill-height align-center justify-center ma-0>
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-layout>
            <v-container fill-height fluid>
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline">Rodrigo<br> Carvalho</span>
                </v-flex>
              </v-layout>
            </v-container>
          </v-img>
          <v-card-title>
            <div>
              <span class="grey--text">Analista em Marketing Digital</span><br>
              <span>10 anos de experi&ecirc;ncia na &aacute;rea.</span><br>
              <span>
                <b>
                  "Sua marca e seus produtos trabalhados da maneira certa!"
                </b>
              </span><br><br><br>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn href="https://rodrigowebcarvalho.com.br/" target="_blank"
              depressed small color="accent"
            >
              Site Pessoal
            </v-btn>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Linkedin
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      <v-flex d-flex xs12 sm6 md4 lg4>
        <v-card contain>
          <v-img
            class="dark--text"
            height="350px"
            src="/static/aulus1.jpeg"
          >
            <v-container fill-height fluid>
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline">Aulus<br> Diniz</span>
                </v-flex>
              </v-layout>
            </v-container>
          </v-img>
          <v-card-title>
            <div>
              <span class="grey--text">Engenheiro de Software</span><br>
              <span>Formado na Universidade de Bras&iacute;lia, curso nota 5 no MEC.</span><br>
              <span><b>"Ser engenheiro &eacute; ser capaz de construir o que eu quiser."</b></span><br><br>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Facebook
            </v-btn>
            <v-btn href="#" target="_blank"
              depressed small color="accent"
            >
              Linkedin
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  'name': 'Team'
}
</script>

<style scoped lang="css">

</style>
