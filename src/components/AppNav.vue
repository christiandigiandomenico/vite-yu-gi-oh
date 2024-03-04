<script>

export default {

    name: "AppNav"

}

</script>

<template>

<nav class="nav-element">

    <img src="../../public/yu-gi-oh.png" alt="Yu-Gi-Oh Logo">

    <h2>Yu-Gi-Oh Api</h2>

</nav>

</template>

<style lang="scss">

nav {
    height: 100px;
    background-color: white;
    display: flex;
    align-items: center;
    gap: 20px;
    img {
        width: 75px;
        height: 75px;
        margin-left: 25px;
    }
    h2 {
        color: black;
        font-size: 40px;
        font-weight: 500;
    }
}

</style>