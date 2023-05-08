<script>

export default {
    name: 'CardComp',
    props: ['tipoCarta']
}
</script>

<template>
    <div class="card">
        <img :src="tipoCarta.card_images[0].image_url" alt="">
        <div>
            <h5>{{ tipoCarta.name }}</h5>
            <span>{{ tipoCarta.archetype }}</span>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    background-color: rgb(212 143 56);

    border: 0px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    margin: 20px;
    padding: 10px;
    width: 200px;

    img {
        height: 200px;
        width: 150px;
    }
}
</style>