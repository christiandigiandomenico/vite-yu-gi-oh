<script>
export default {
    name: 'AppCard',

    props: {
        card: Object,
    },
}
</script>

<template>
    <li class="card">
        <img :src="card.card_images.image_url_small" :alt="card.name">
        {{ card.name }}
    </li>
</template>

<style lang="scss">


</style>