<script setup>
import { RouterView } from 'vue-router';
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';
import { useRoute } from 'vue-router'

const route = useRoute()
</script>

<template>
  <TheHeader v-if="route.name !== 'not-found'" />
    <main>
      <RouterView />
    </main>
  <TheFooter v-if="route.name !== 'not-found'" />
</template>