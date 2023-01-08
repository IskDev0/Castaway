<template>
  <section class="latest section">
    <div class="container">
      <div class="episodes">
        <div class="episode" v-for="episode in reversedEpisodes" :key="episode.id">
          <img :src="episode.image" alt="podcast image">
          <div class="episode__text">
            <p class="episode__genre">{{ episode.genre }}</p>
            <p class="episode__number section__subtitle">Episode {{ episode.id }}</p>
            <p class="episode__title">{{ episode.title }}</p>
            <p class="episode__desc desc">{{ episode.desc }}</p>
            <button class="episode__btn">View Episode Details</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import data from "../data";
import {computed} from "vue";

let latest = data.slice(0, 3)

let reversedEpisodes = computed(() => {
  return latest.slice(0).reverse()
})


</script>

