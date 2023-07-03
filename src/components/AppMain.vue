<script>
import { store } from '../data/store';

export default {
    data() {
        return { store }
    }
}
</script>

<template>
    <div class="container">
        <div v-for="character in store.characters" class="card">
            <img :src="character.imageUrl" class="card-img-top" :alt="character.name">
            <div class="card-body">
                <h5 class="card-title">{{ character.name }}</h5>
                <p class="card-text">
                    Type : {{ character.type1 }}
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-wrap: wrap;
}

.card {
    margin: 0 auto;
    width: 18rem;
    margin: 10px;
}

.card-img-top {
    height: 200px;
    width: 250px;
    object-fit: contain;
}
</style>