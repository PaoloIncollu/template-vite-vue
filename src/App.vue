<script>
/* 
  Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
  1) Importazione del componente
  2) Dichiarazione del componente
  3) Utilizzo del componente
*/
// 1) Importazione del componente
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';
import { store } from './store.js';
export default {
  data() {
    return { 
      
    }
  },
  // 2) Dichiarazione del componente
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  methods: {
    
  }/*,
created() {
    axios
      .get(...)
      .then((res) => {
        console.log('OGGETTO CREATO DA AXIOS:', res);
        console.log('DATI CHE CI HA RISPOSTO IL SERVER:', res.data);
        console.log('TUTTI I PERSONAGGI:', res.data.results);

        this.store.allCharacters = res.data.results;
      });
  }*/
}
</script>

<template>
  <div>
    <!-- 3) Utilizzo del componente -->
    <AppHeader />
    
    <AppMain/>

    <AppFooter/>
  </div>
</template>

<style lang="scss">
@use '../src/assets/scss/main.scss' as *;

// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
</style>
