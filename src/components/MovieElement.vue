<template>
    <div>
        <h4> {{ movie.title }} </h4>
        <h5> {{ movie.original_title }} </h5>
        <p> {{ movie.original_language}}</p>
        <p> {{ movie.vote_average }} </p>
        <hr>
    </div>
</template>

<script>
export default {
    props:{
        // Sono i dati che mi arrivano da Main.vue
        'movie': {
            type: Object,
            required: true,
        }
    },
}
</script>

<style>

</style>