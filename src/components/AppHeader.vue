<script>
export default {
    emits: ['selectChange'],
    data() {

        return {
            selected: '',
            types: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ]
        }
    },
    methods: {
        // metodo che trasmette il value della select al padre
        onChange() {
            this.$emit('selectChange', this.selected)
        }
    }
}
</script>

<template>
    <header class="container">
        <h1 class="text-center margin-0-auto my-3">Pokédex</h1>
        <nav>
            <div class="my-3">Ordina per tipo</div>
            <select class="form-select" @change="onChange" v-model="selected">
                <option selected value="">Visualizza tutti</option>
                <option v-for="ability in types" :value="ability"> {{ ability }} </option>
            </select>
        </nav>
    </header>
</template>