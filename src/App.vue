<script>
import axios from 'axios';
import { store }  from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';
import AppSearch from './components/AppSearch.vue';

export default {
  components: {
    AppHeader,
    CardList,
    AppSearch
  },

  data() {
    return {
      store,
      cardArray : []
    }
  },

  created() {
    axios.get('https://rickandmortyapi.com/api/character').then((resp) => {
      this.cardArray = resp.data.results;
      console.log(this.cardArray);
    })
  },
  methods: {
    filter() {
      console.log('filter', this.store.statusValue);
    }
  }
}
</script>

<template>
  <AppHeader />
  <AppSearch @changeValue="filter"/>
  <CardList :cardArray = 'cardArray'/>

</template>

<style lang="scss">

</style>
