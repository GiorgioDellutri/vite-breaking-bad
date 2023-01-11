<script>
import { store } from '../store';
import axios from 'axios';


export default {
    name: 'AppMain',
    data() {
        return {
            store,
        }
    },
    methods: {
        getImage() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0', {
                params: {
                }
            })
                .then(function (response) {
                    console.log(response);
                })
                .catch(function (error) {
                    console.log(error);
                })
        }
    },

    created() {
        this.getImage()
    },
}
</script>

<template>
    <div>
        <h1>Main</h1>
        <p>
            {{ store.searchText }}
        </p>
    </div>
</template>


<style lang="scss" scoped>

</style>