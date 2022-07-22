<template>
    <div>
        <!-- Stampami MovieElement tante volte quante sono gli elementi dentro movies -->
        <!-- Passo a MovieElement il singolo elemento di movies -->
        <!-- movies  è un array di oggetti, movie è un oggetto -->
        <MovieElement class="container" v-for="(movie, index) in movies" :key="index" :movie="movie"/>
    </div>
</template>

<script>
import MovieElement from './MovieElement.vue'

export default {
    props: {
        // Sono i dati che mi arrivano da App.vue
        'movies': {
            type: Array,
            required: true,
        }
    },

    components: {
        MovieElement,
    },
}
</script>

<style>

</style>