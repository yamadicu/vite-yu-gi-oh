<script>
import { store } from '../store'
import CardComp from './CardComp.vue';
export default {
    name: 'MainComp',
    components: {
        CardComp
    }, data() {
        return {
            store
        }
    }
}
</script>

<template>
    <!-- PARTE CON SFONDO ARANCIONE E SELEZIONE DELLA CARTA -->
    <div id="back-generale">
        <div class="contenuto">

            <div id="selezione">

                <div class="dropdown">
                    <a class="btn btn-secondary dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                        aria-expanded="false">
                        Alien
                    </a>
                </div>
            </div>
            <!-- SEZIONE CHE CONTERRA LE CARTE -->
            <div id="sez-card" class="scroll">
                <CardComp v-for="(element, index) in store.arrayCarte" :key="index" :tipoCarta="element" />

            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
#back-generale {
    height: 90vh;
    background-color: rgb(212 143 56);



    .contenuto {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        #selezione {
            padding-top: 10px;
            display: flex;
            align-items: flex-start;
        }

        #sez-card {
            background-color: white;
            width: 80vw;
            height: 80vh;
            margin-top: 20px;
            display: flex;
            flex-wrap: wrap;
            overflow: auto;
        }

    }
}
</style>