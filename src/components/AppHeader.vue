<script>
import { store } from '../data/store';
export default {

    data() {
        return { store }
    },
}
</script>

<template>
    <header class="container">
        <h1 class="text-center margin-0-auto my-3">Pokédex</h1>
        <nav>
            <div class="my-3">Ordina per tipo</div>
            <select class="form-select">
                <option selected>Visualizza tutti</option>
                <option v-for="char in store.characters" :value="char.type1"> {{ char.type1 }} </option>
            </select>
        </nav>
    </header>
</template>

<style></style>