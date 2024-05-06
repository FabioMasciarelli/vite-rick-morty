<script>
import PropsCard from './PropsCard.vue';

export default {
    components: {
        PropsCard,
    },

    data() {
        return {

        }
    },

    props: {
        cardArray: Array
    }
}
</script>

<template>
    <div class="container">
        <div class="row ms-row">
            <div class="col" v-for="card in cardArray">
                <PropsCard :cardInfo="card"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>
