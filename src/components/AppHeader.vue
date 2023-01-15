<script>
import axios from 'axios';
import { store } from '../store';

export default {
    name: 'AppHeader',
    data() {
        return {
            store
        }
    },
    methods: {
        getCardList() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0', {
                params: {
                }
            })
                .then((response) => {
                    console.log(response.data.data);
                    this.store.cardList = response.data.data;
                    console.log(this)

                })
                .catch(function (error) {
                    console.log(error);
                })
        }
    },

    created() {
        this.getCardList()
    },
}
</script>

<template>
    <header>
        <img src="../assets/img/Yu-Gi-Oh logo.webp" alt="logo">
    </header>
    <div class="count-banner">
        <p class="card-count">Found {{ store.cardList.length }} card</p>
    </div>
</template>


<style lang="scss" scoped>
header {
    display: flex;
    height: 10vh;
    padding: 1rem;
    font-size: 1.5rem;

    img {
        margin-left: .5rem;
        height: 100%;
        line-height: 10px;
    }
}

div.count-banner {
    padding: 1rem;
    background-color: #212529;

    p.card-count {
        font-size: 1.5rem;
        color: whitesmoke;
    }
}
</style>