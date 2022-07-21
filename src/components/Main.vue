<template>
    <div>
        <!-- Stampami DiscElement tante volte quante sono gli elementi dentro discs -->
        <!-- Passo a DiscElement il singolo elemento di discs -->
        <!-- discs è un array di oggetti, disc è un oggetto -->
        <MovieElement class="container" v-for="(movie, index) in movies" :key="index" :movie="movie"/>
    </div>
</template>

<script>
import MovieElement from './MovieElement.vue'

export default {
    props:{
        // Sono i dati che mi arrivano da App.vue
        'movies': {
            type: Array,
            required: true,
        }
    },

    components:{
        MovieElement,
    },
}
</script>

<style>

</style>