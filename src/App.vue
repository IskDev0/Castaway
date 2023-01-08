<script setup>
import {RouterView} from 'vue-router'
import TheHeader from "./components/TheHeader.vue"
import TheHero from "./components/TheHero.vue"
import LatestEpisodes from "./components/LatestEpisodes.vue";
import AboutSection from "./components/AboutSection.vue"
</script>

<template>
  <TheHeader/>
  <TheHero/>
  <LatestEpisodes/>
  <AboutSection/>
  <RouterView/>
</template>
