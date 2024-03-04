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
        <img :src="card.card_images[0].image_url_small" :alt="card.name">
        <span class="card-name">{{ card.name }}</span>
        <span class="card-type">{{ card.type }}</span>
    </li>
</template>

<style lang="scss">

.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    
    background-color: #d48f38;

    width: calc(100% / 5);

    img {
        height: 150px;
        width: 100px;
    }

    .card-type {
        color: black;
    }
}

</style>