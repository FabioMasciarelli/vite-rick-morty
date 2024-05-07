<script>
import { store }  from '../store.js';

export default {
    props: {
        cardInfo: Object
    },

    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div class="card ms-card" v-if="cardInfo.status === store.statusValue">
        <img :src="cardInfo.image" alt="">
        <div class="card-body">
            <h4>{{ cardInfo.name }}</h4>
            <p>{{ cardInfo.status }}</p>
            <p>{{ cardInfo.species }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    
</style>