<script>
import axios from 'axios';
import { store } from './store';
import HeaderComp from './components/HeaderComp.vue';
import MainComp from './components/MainComp.vue';
export default {
  name: 'app',
  components: {
    HeaderComp,
    MainComp
  },
  data() {
    return {
      store
    }
  },
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
      .then((res) => {
        console.log(res.data.data);

        const datiCard = res.data.data

        this.store.arrayCarte = datiCard
      })
  }
}
</script>

<template>
  <HeaderComp />
  <MainComp />
</template>

<style lang="scss">
@use './style/main.scss';
</style>
