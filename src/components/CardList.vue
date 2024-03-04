<script>

import {store} from '../store.js';

import AppCard from './AppCard.vue'

export default {
    name: 'CardList',

    components:  {
        AppCard,
    },

    data() {
        return  {
            store,
        }
    }
}
</script>

<template>

    <div class="container">

        <ul>
            
            <AppCard v-for="currentCard in store.cards" :card="currentCard"></AppCard>
           
        </ul>

    </div>

</template>

<style lang="scss">

.container {
    height: calc(100vh - 100px);
    background-color: #d48f38;
};

</style>