<template>
    <button @click="go_to_fullpage" class="card">
        <img :src="image">
        <h1>{{ titre }}</h1>
    </button>
</template>

<script>
export default{
    props:{
        titre: String,
        image: String
    },
    methods:{
        go_to_fullpage(){
            console.log("click");
            this.$router.push(`/recette/${this.titre}`)
        }
    }
}
</script>

<style scoped>
    .card {
    display: block;  /* Rend le lien cliquable sur toute la zone */
    text-decoration: none;  /* Supprime le soulignement par défaut */
    background-color: lightgray;  /* Optionnel : fond du lien */
    border-radius: 8px;
    padding: 15px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease-in-out;
    }

    .card:hover {
    transform: scale(1.05);  /* Effet d'agrandissement au survol */
    }

    .card-img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
    }

    .card-title {
    font-size: 1.2em;
    text-align: center;
    margin-top: 8px;
    }

    .card:hover {
    cursor: pointer;  /* Curseur pointer pour indiquer que c'est cliquable */
    }
</style>

