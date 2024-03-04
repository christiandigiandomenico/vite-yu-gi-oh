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
      }
    },

  created() {
    
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0').then(res => {
        console.log(res.data.data)
        this.store.cards = res.data.data
    })

  },
  
  components: {
    AppNav,
    CardList
  }

}

</script>

<template>

<AppNav></AppNav>

<CardList></CardList>
  
</template>

<style>

</style>
