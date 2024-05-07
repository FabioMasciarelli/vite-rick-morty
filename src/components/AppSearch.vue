<script>

import { store }  from './../store.js';

export default {

    data() {
        return {
            store,
            statusList: ['Dead', 'Alive', 'unknown'],
        }
    }
}
</script>

<template>
    <div>
        <select @change="$emit('changeValue')" v-model="store.statusValue">
            <option :value="item" v-for="item in statusList">{{ item }}</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>

</style>