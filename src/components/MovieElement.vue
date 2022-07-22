<template>
    <div>
        <ul class="list-group mb-3">
            <li class="list-group-item"> {{ movie.title }} </li>
            <li class="list-group-item"> {{ movie.original_title }} </li>
            <li class="list-group-item"> <lang-flag :iso="movie.original_language"/> </li>
            <li class="list-group-item"> {{ movie.vote_average }} </li>
        </ul>
    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {

    components: {
        LangFlag,
    },
  
    props: {
        // Sono i dati che mi arrivano da Main.vue
        'movie': {
            type: Object,
            required: true,
        }
    },

    methods: {

    },
}

</script>

<style>

</style>