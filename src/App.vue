<script>

import AppMain from './components/AppMain.vue';

import axios from 'axios';

//Importo store dove sono contenuti i miei dati provenienti dal API
import { store } from './data/store';

// importo API in costante endpoint
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=1048';

export default {
  components: { AppMain },
  data() {
    return {
      searchAbility: '',
    }
  },
  methods: {
    // metodo che riceve il dato dal emit
    search(data) {
      this.searchAbility = data

    }
  },
  //utilizzo axios per importare i dati
  created() {
    axios.get(endpoint).then(res => {
      store.characters = res.data.docs;
    });
  }
};
</script>

<template>
  <AppMain @abilitySearch="search" />
</template>

<style lang="scss">
@use './assets/style.scss';
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
