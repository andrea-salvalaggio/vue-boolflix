<template>
    <div class="container">
        <!-- Stampami MovieElement tante volte quante sono gli elementi dentro movies -->
        <!-- Passo a MovieElement il singolo elemento di movies -->
        <!-- movies  è un array di oggetti, movie è un oggetto -->
        <MovieElement v-for="(movie, index) in movies" :key="index" :movie="movie"/>
        <TvShowElement v-for="(tvshow, index) in tvshows" :key="index" :tvshow="tvshow"/>
    </div>
</template>

<script>
import MovieElement from './MovieElement.vue'
import TvShowElement from './TvShowElement.vue'

export default {
    props: {
        // Sono i dati che mi arrivano da App.vue
        'movies': {
            type: Array,
            required: true,
        },

        'tvshows': {
            type: Array,
            required: true,
        },
    },

    components: {
        MovieElement,
        TvShowElement,
    },
}
</script>

<style>

</style>