<script>

import {store} from '../store.js';

import AppCard from './AppCard.vue';
import AppCounter from './AppCounter.vue'

export default {
    name: 'CardList',

    components:  {
        AppCard,
        AppCounter
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

        <div class="card-container">

            <AppCounter></AppCounter>

            <ul>
            
                <AppCard v-for="currentCard in store.cards" :card="currentCard"></AppCard>
           
            </ul>

        </div>

    </div>

</template>

<style lang="scss">

.container {
    height: calc(100vh - 100px);
    background-color: #d48f38;
    padding: 20px;

    .card-container {
        background-color: white;
        padding: 50px
    }

    ul {
        list-style-type: none;
        display: flex;
        flex-wrap: wrap;
        
    }
};

</style>