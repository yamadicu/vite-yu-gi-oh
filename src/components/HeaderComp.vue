<script>
export default {
    name: 'HeaderComp'
}
</script>

<template>
    <nav>
        <img src="/img/yugioh.svg" alt="">
        <span>Yu-Gi-Oh Api</span>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    height: 100px;
    background-color: white;

    img {
        height: 10vh;
        padding: 20px;
    }

    span {
        font-size: 2rem;
        font-weight: bold;
    }
}
</style>