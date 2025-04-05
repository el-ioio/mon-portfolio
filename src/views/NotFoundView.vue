<template>
    <div class="centrer">
        <h1>Erreur 404</h1>
        <p>Il n'y a rien ici</p>
        <img src="@/assets/image/erreur-404.jpg" alt="Erreur 404">
        <RouterLink to="/">Retour</RouterLink>
    </div>
</template>

<script setup>
import { RouterLink } from 'vue-router';
</script>

<style scoped>
.centrer {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
    padding-left: 300px;
}

h1 {
    font-size: 300%;
}

p {
    font-size: 150%;
}
</style>