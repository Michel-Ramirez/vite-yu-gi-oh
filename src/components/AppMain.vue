<script>
export default {
    props: {
        pokemonList: Array
    }
}
</script>

<template>
    <div class="container">
        <div v-for="pokemon in pokemonList" class="card">
            <img :src="pokemon.imageUrl" class="card-img-top" :alt="pokemon.name">
            <div class="card-body">
                <h5 class="card-title">{{ pokemon.name }}</h5>
                <p class="card-text">
                    Type : {{ pokemon.type1 }}
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