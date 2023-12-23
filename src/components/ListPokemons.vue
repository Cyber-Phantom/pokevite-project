<template>
    <div class="col-4">

        <div class="card p-2 mb-3 cardListPokemon">
            <p class="text-center">{{ pokemon.name }}</p>
            <img :src="urlBaseSvg" class="card-img-top" alt="..." height="80">
        </div>

    </div>
</template>

<script setup lang="ts">
const pokemon = defineProps(["name", "urlBaseSvg"])

</script>

<style scoped>

.cardListPokemon {
    background: rgb(28, 38, 153);
    background: radial-gradient(circle, rgba(15, 28, 165, 0.505) 0%, rgba(70, 252, 243, 0.705) 100%);
    cursor: pointer;
}

.cardListPokemon:hover {
    background: rgb(28, 38, 153);
    background: radial-gradient(circle, rgba(15, 28, 165, 0.7) 0%, rgba(70, 252, 243, 0.9) 100%);
    cursor: pointer;
}

.cardListPokemon img:hover {
    padding: .2rem;
}

</style>
