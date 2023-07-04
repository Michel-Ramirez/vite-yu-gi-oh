<script>

import AppMain from './components/AppMain.vue';

import axios from 'axios';

//Importo store dove sono contenuti i miei dati provenienti dal API
import { store } from './data/store';

// importo API in costante endpoint
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc';

export default {
  components: { AppMain },
  data() {
    return {
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
  <AppMain />
</template>

<style lang="scss">
@use './assets/style.scss';
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
