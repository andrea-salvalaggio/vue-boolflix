<template>
    <div>
        <h1> {{ movie.title }} </h1>
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