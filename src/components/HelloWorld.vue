<template>
  <div class="hello">
    <h1>Nova Era Solu&ccedil;&otilde;es Digitais</h1>
    <h2>Essential Links</h2>
    <Carousel></Carousel>
  </div>
</template>

<script>
import Carousel from './Carousel'
export default {
  name: 'HelloWorld',
  components: {
    'Carousel': Carousel
  },
  data () {
    return {
      msg: 'Nova Era Solu&ccedil;&otilde;es Digitais'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
