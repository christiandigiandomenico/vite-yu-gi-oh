<script>
import {store} from '../store.js';

export default {
    name: 'AppCounter',


    data() {
        return {
            store,
        }
    }

}

</script>

<template>

<span>
    <div class="container-counter">
        Card found: {{ store.cards.length }}
    </div>
</span>

</template>

<style lang="scss">

.container-counter {
    background-color: #212529;
    color: white;
    width: 100%;
    font-size: 20px;
    font-weight: bold;
    padding: 15px;
}

</style>