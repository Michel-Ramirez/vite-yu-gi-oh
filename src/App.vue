<script>

import AppMain from './components/AppMain.vue';
import axios from 'axios';

const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc';

export default {
  components: { AppMain },
  data() {
    return {
      characters: []
    }
  },
  created() {
    axios.get(endpoint).then(res => {
      this.characters = res.data.docs;
    });
  }
};
</script>

<template>
  <h1 class="text-center margin-0-auto mt-5">POKEDESC</h1>
  <AppMain :pokemonList="characters" />
</template>

<style lang="scss">
@use './assets/style.scss';
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
