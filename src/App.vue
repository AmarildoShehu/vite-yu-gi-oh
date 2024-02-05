<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
import AppMain from './components/AppMain.vue';
import { store } from './data/store.js';
export default {
  name: 'Pokedex',

  components: {
    AppMain
  },
  created() {
    axios.get(endpoint).then(res => {
      store.listPokemon = res.data.docs;
    })
  }
};
</script>

<template>
  <AppMain />
</template>

<style lang="scss" scoped>
@use './assets/scss/style.scss'
</style>