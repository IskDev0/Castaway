<template>
  <section id="episodes" class="latest section">
    <div class="container">
      <div class="episodes">
        <EpisodeItem :episode="episode" class="episode" v-for="episode in reversedEpisodes" :key="episode.id"/>
      </div>
    </div>
  </section>
</template>

<script setup>
import data from "../data";
import {computed} from "vue";
import EpisodeItem from "./EpisodeItem.vue";

let latest = data.slice(0, 3)

let reversedEpisodes = computed(() => {
  return latest.slice(0).reverse()
})


</script>

