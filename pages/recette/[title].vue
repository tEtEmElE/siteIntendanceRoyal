<template>
    <div>
      <h1>{{ route.params.title }}</h1>
      <div v-for="recette in lst_recette" :key="recette.Title">
        <div v-if="recette.Title === route.params.title">
          <p>Ingrédients: {{ recette.Ingredient }}</p>
          <p>Matériel: {{ recette.Materielle }}</p>
          <p>Étapes:</p>
          <ul>
            <li v-for="(etape, index) in recette.Etape" :key="index">{{ etape }}</li>
          </ul>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { useRoute } from 'vue-router';
  
  const route = useRoute();
  
  const lst_recette = [
    {
      Title: "Faire des frites maison",
      Ingredient: "Patates",
      Materielle: "Friteuse",
      Image: "https://www.specialgastronomie.com/recette-de-graisse-de-boeuf-pour-frites",
      Etape: {
        1: "Couper les frites",
        2: "Faire une précuisson dans la friteuse",
        3: "Faire la cuisson finale et déguster"
      }
    }
  ];
  </script>
  