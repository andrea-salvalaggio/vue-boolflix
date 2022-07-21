<template>
    <div>
        Main
        <DiscElement v-for="(disc, index) in discs" :key="index"/>
    </div>
</template>

<script>
import DiscElement from './DiscElement.vue'

export default {
    props:{
        'discs': {
            type: Array,
            required: true,
        }
    },

    components:{
        DiscElement,
    },
}
</script>

<style>

</style>