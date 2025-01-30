<template>
    <nav>
        <ul>
            <li>
                <NuxtLink to="/">Acceuil</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/recette">Recette</NuxtLink>
            </li>
        </ul>
    </nav>
</template>


<style scoped>
    nav{
        background-color: gray;
        width: 100%;
        display: flex;
        justify-content: space-between;
    }
</style>
