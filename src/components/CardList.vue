<script>
import { store } from '../store';
import SingleCard from './SingleCard.vue';


export default {
    name: 'CardList',
    props: {

    },
    components: {
        SingleCard
    },
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <SingleCard v-for="singleCard in store.cardList" :cards="singleCard" />
</template>
