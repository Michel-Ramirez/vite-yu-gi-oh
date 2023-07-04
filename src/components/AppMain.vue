<script>
import CardComponent from './CardComponent.vue';
import AppHeader from './AppHeader.vue';
export default {
    components: { AppHeader, CardComponent }
}
</script>

<template>
    <div class="container mt-5">
        <div class="pokedex-body">
            <div class="pokedex-border-screen">
                <div class="notch">
                    <div class="camera-sensor"></div>
                </div>
                <AppHeader />
                <CardComponent />
            </div>

        </div>
    </div>
</template>

<style scoped>
.container {
    max-width: 820px;
}

.pokedex-body {
    border: 15px solid red;
    border-radius: 20px;
}

.pokedex-border-screen {
    border: 5px solid black;
    height: 1100px;
    overflow: auto;
    display: flex;
    align-items: center;
    flex-direction: column;
}

::-webkit-scrollbar {
    width: 0px;
}

.notch {
    width: 100px;
    height: 50px;
    background-color: rgb(0, 0, 0);
    border-radius: 0 0 10px 10px;
    display: flex;
    justify-content: end;
}

.camera-sensor {
    margin: 5px 0;
    margin-right: 10px;
    height: 10px;
    width: 10px;
    border-radius: 50%;
    background-color: rgba(30, 29, 29, 0.657);
}
</style>