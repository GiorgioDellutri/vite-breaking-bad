<script>
import { store } from '../store';
import AppCard from '../components/AppCard.vue';



export default {
    name: 'AppMain',

    components: {
        AppCard
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
        <AppCard v-for="card in store.cardList" :singleCard="card" />
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




// div.count-banner {
//     padding: 1rem;
//     background-color: #212529;

//     p.card-count {
//         font-size: 1.5rem;
//         color: whitesmoke;
//     }
// }

// div.card-container {
//     display: flex;
//     flex-wrap: wrap;
//     border: 15px solid #212529;
//     border-radius: 20px;
//     max-width: 1300px;
//     margin: 0 auto;
//     margin-top: 2rem;
//     padding: 1rem;
//     text-align: center;
//     font-weight: 500;

//     div.card {
//         width: calc(100% / 5 - 2rem);
//         border: 4px solid #212529;
//         border-radius: 10px;
//         background-color: whitesmoke;
//         padding: .8rem;
//         margin: 1rem;

//         img {
//             width: 100%;
//         }

//         p.card-name {
//             margin-top: 1rem;
//         }
//     }
// }