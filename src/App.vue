<template>
  <div id="app">
    <!-- App rimane in ascolto del segnale startSearch del componente Header e quando avviene richiamo la funzione getMovies -->
    <Header @startSearch="getMovies"/>
    <!-- Passo i risultati a Main tramite props -->
    <Main :movies="movies"/>
    
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },

  data: function() {
    return{
      movies: [],
      apiUrl: 'https://api.themoviedb.org/3/search/movie/?api_key=eb7d21fbf7495f073ee3484c1c5e2b66&query=',
    }
  },

  methods: {
    getMovies: function(searchText) {
      // Questa funzione viene chiamata quando avviene l'evento startSearch e riceve come parametro il testo che l'utente ha scritto nell'input
      console.log(searchText);
      // Faccio partire la chiamata axios
      axios.get(this.apiUrl + searchText)
        .then((result) => {
          console.log(result.data.results);
          // Assegno il contenuto .data.results all'array inizialmente vuoto (disc)
          this.movies = result.data.results;
        })
        .catch((error) => {
          console.log(error);
        });
    }
  },

  // created() {
  //   this.getMovies();
  // },

}
</script>

<style lang="scss">
  @import "~bootstrap/scss/bootstrap.scss";

</style>
