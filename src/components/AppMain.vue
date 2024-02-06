<script>
import { store } from '../data/store.js'
import PokemonCard from './PokemonCards.vue';
export default {
    name: 'AppMain',
    data: () => ({
        store
    }),
    components: {
        PokemonCard
    }
}
</script>

<template>
    <main>

        <div class="container">
            <div class="row justify-content-center">
                <div class="col col-lg-2 m-1" v-for="pokemon in store.listPokemon">
                    <PokemonCard :pokemon="pokemon" />
                </div>
            </div>
        </div>
    </main>
</template>



<style lang="scss" scoped>
main {
    background-color: #B71B1B;
}
</style>

