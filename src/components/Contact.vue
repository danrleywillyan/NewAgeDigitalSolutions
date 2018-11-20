<template>
<Form></Form>
</template>

<script>
import Form from './Form'
export default {
  name: 'Contact',
  components: {
    'Form': Form
  },
  data () {
    return {
      msg: 'Temos o prazer de apresentar nosso time.'
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
