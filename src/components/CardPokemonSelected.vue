<template>
    <div>

        <div class="card CardPokemonSelected" :class="loading ? '' : 'animate__animated animate__flipInY'">

            <img v-if="name" :src="img" class="card-img-top pt-2" :alt="name">
            <img v-else src="@/assets/egg_pokemon.svg" class="card-img-top pt-2" alt="???">

            <div class="card-body">
                <h5 class="card-title text-center">{{ name || '???' }}</h5>
                <hr>
                <div class="row">
                    <section class="col">
                        <strong>XP: </strong>
                        <span>{{ xp }}</span>
                    </section>
                    <section class="col">
                        <strong>Altura: </strong>
                        <span>{{ height }}</span>
                    </section>
                </div>
            </div>
        </div>

    </div>
</template>

<script setup lang="ts">

defineProps(['name', 'xp', 'height', 'img', 'loading'])

</script>

<style scoped>
.CardPokemonSelected {
    height: 75vh;
    background: rgb(10, 28, 112);
    background: radial-gradient(circle, rgba(197, 129, 50, 0.8) 0%, rgba(209, 5, 5, 0.8) 100%);
}

.CardPokemonSelected img {
    height: 250px;
}

@media (max-width: 768px) {
    .CardPokemonSelected {
        height: 35vh;
        width: 48%;
        margin: 0 auto 10px auto;
    }

    .CardPokemonSelected img {
        height: 100px;
    }
}
</style>
