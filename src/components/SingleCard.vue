<script>
import { store } from '../store';


export default {
    name: 'SingleCard',
    props: {
        cards: {
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
    <div class="card-container">
        <div class="card-image">
            <img :src="cards.card_images[0].image_url" :alt="cards.name">
            <p class="card-name">
                {{ cards.name }}
            </p>
            <p class="card-archetype">
                {{ cards.archetype }}
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
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