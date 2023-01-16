<script>
import { store } from '../store';
import CardList from './CardList.vue';

export default {
    name: 'AppMain',

    components: {
        CardList
    },
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <main>
        <CardList />
    </main>
</template>


<style lang="scss" scoped>
main {
    display: flex;
    flex-wrap: wrap;
    max-width: 1300px;
    margin: 0 auto;
}
</style>
