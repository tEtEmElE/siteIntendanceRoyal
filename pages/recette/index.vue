<template>
    <div>
        <h1>Recette</h1>
        <p>{{ recette }}</p>
        <div v-for="recette in Object.values(lst_recette._value.Frite)">
            <FicheRecette :titre="recette[0]" :image="recette[3]" />
        </div>
    </div>
</template>

<script>
import FicheRecette from '~/components/FicheRecette.vue';
import { useFetch } from '#app'

const { data: lst_recette } = await useFetch("/api/getRecettes")
// lst_recette = recettes._value.Frite
console.log(Object.values(lst_recette._value.Frite))

export default {
    components: {
        FicheRecette
    }
};
</script>