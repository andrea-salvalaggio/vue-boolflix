<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-12 mt-5">
                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="Cerca un film o una serie" v-model.trim="text" @keyup.enter="$emit('startSearch', text)">
                        <!-- Quando l'utente clicca il componente Header lancia il segnale startSearch passando il testo inserito dall'utente -->
                        <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="$emit('startSearch', text)">Cerca</button>
                    </div>
                </div>
            </div>
        </div>     
    </header>
</template>

<script>

export default {

    data: function(){
        return{
            text: '',
        }
    },

    methods: {
        // isClicked: function(){
        //     console.log(this.text);
        // }
    },
}
</script>

<style lang="scss" scoped>

    input:placeholder-shown {
        font-style: italic;
    }

</style>