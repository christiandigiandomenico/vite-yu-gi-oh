<script>

import axios from 'axios';

import {store} from './store'

import AppNav from './components/AppNav.vue';
import CardList from './components/CardList.vue'

export default {

  data() {
      return {
        cards: [],

        store,

        isLoading: true,
      }
    },

  created() {
    
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0').then(res => {
        console.log(res.data.data)
        this.store.cards = res.data.data
        this.isLoading = false;
    })

  },
  
  components: {
    AppNav,
    CardList
  }

}

</script>

<template>

<div v-if="isLoading" class="splash-page">
  <img src="../public/yu-gi-oh.png" alt="Yu-Gi-Oh Logo">
  <h1>Loading...</h1>
</div>

<div v-else>

  <AppNav></AppNav>

  <CardList></CardList>

</div>
  
</template>

<style>

.splash-page {
  text-align: center;
}

</style>
