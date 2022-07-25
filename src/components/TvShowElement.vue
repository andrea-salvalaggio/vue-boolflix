<template>
  <div>
        <ul class="list-group mb-3">
            <li class="list-group-item"> {{ tvshow.name }} </li>
            <li class="list-group-item"> {{ tvshow.original_name }} </li>
            <li class="list-group-item"> <lang-flag :iso="tvshow.original_language"/> </li>
            <li class="list-group-item"> {{ tvshow.vote_average }} </li>
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
        'tvshow': {
            type: Object,
            required: true,
        }
    },

}
</script>

<style>

</style>