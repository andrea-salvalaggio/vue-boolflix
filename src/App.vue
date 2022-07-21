<template>
  <div id="app">
    <Header/>
    <Main :discs="discs"/>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },

  data: function() {
    return{
      discs: [
        "uno",
        "due",
        "tre",
      ],

      apiUrl: ''
    }
  },
}
</script>

<style lang="scss">
  @import "~bootstrap/scss/bootstrap.scss";

</style>
