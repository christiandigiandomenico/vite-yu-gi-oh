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
    <select name="archetype" id="selector" @change="$emit('search')" v-model="store.archetypeCard">
        <option value="">Seleziona un'opzione</option>
        <option v-for="currentArch in store.archetype" :value="currentArch.archetype_name">{{ currentArch.archetype_name }}</option>
    </select>
</div>

</template>

<style lang="scss">



</style>