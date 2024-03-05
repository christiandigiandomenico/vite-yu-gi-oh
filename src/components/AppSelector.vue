<script>

import {store} from '../store.js';

export default {

    name: "AppSelector",

    data() {
    return {
      store,
    }
  },

}

</script>

<template>

<div id="search-bar">
    <select name="archetype" id="selector" @change="$emit('search')">
        <option value="">Seleziona un'opzione</option>
        <option v-for="currentArch in store.archetype" value="archetype">{{ currentArch }}</option>
    </select>
</div>

</template>

<style lang="scss">



</style>