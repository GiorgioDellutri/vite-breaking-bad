<script>
import { store } from '../store';

export default {
    name: 'AppCard',
    props: {
        singleCard: {
            type: Object,
            required: true,
        }
    },

    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <!-- <div class="count-banner">
        <p class="card-count">Found {{ singleCard.length }} card</p>
    </div> -->
    <div class="card-container">
        <div class="card-image">
            <img :src="singleCard.card_images[0].image_url" :alt="singleCard.name">
            <p class="card-name">
                {{ singleCard.name }}
            </p>
            <p class="card-archetype">
                {{ singleCard.archetype }}
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
// div.count-banner {
//     padding: 1rem;
//     background-color: #212529;

//     p.card-count {
//         font-size: 1.5rem;
//         color: whitesmoke;
//     }
// }

div.card-container {
    width: calc(100% / 5 - 2rem);
    border-radius: 10px;
    border: 4px solid #212529;
    padding: 1rem;
    background-color: whitesmoke;
    padding: .8rem;
    margin: 1rem;

    div.card-image {

        img {
            width: 100%;
        }

        p.card-name,
        p.card-archetype {
            text-align: center;
            margin-top: 1rem;
        }
    }
}
</style>