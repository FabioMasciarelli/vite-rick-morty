<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';

export default {
  components: {
    AppHeader,
    CardList
  },

  data() {
    return {
      cardArray : []
    }
  },

  created() {
    axios.get('https://rickandmortyapi.com/api/character').then((resp) => {
      this.cardArray = resp.data.results;
      console.log(this.cardArray);
    });
  }
}
</script>

<template>
  <AppHeader />
  <CardList :cardArray = 'cardArray'/>
</template>

<style lang="scss">

</style>
