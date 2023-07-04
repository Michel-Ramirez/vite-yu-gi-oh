<script>
import { store } from '../data/store';
export default {
    data() {
        return { store }
    },
}
</script>

<template>
    <div class="cards">
        <div v-for="char in store.characters" class="card">
            <img :src="char.imageUrl" class="card-img-top" :alt="char.name">
            <div class="card-body">
                <h5 class="card-title">{{ char.name }}</h5>
                <p class="number">N° : {{ char.number }}</p>
                <p class="card-text">
                    Tipo : {{ char.type1 }}
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.cards {
    display: flex;
    flex-wrap: wrap;
}

.card {
    width: calc(100% / 3 - 20px);
    margin: 10px;
}

.card-img-top {
    height: 300px;
    width: 100%;
    padding: 20px;
    object-fit: contain;
}

.number {
    font-size: 0.8rem;
    color: gray;
    font-weight: 600;
}

.card-text {
    font-size: 0.9rem;
}
</style>