<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from "./components/TheHeader.vue"
import TheHero from "./components/TheHero.vue"
</script>

<template>
  <TheHeader/>
  <TheHero/>
  <RouterView />
</template>
