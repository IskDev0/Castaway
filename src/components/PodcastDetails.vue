<template>
  <section class="details">
    <div class="container">
      <div class="details__wrapper">
        <p class="section__subtitle">{{ sourceData.genre }}</p>
        <p class="section__title">{{ sourceData.title }}</p>
        <div class="details__inner">
          <img :src="image" alt="">
          <p class="details__desc">{{ sourceData.desc.fullBody }}</p>
        </div>
        <div class="details__bottom">
        <p class="episode__genre">{{ sourceData.desc.date }}</p>
          <div class="details__social-wrapper">
            <a href="https://spotify.com" target="_blank" class="details__social-item"><img src="../assets/images/icons/spotify.svg" alt="spotify"></a>
            <a href="https://pocketcasts.com" target="_blank" class="details__social-item"><img src="../assets/images/icons/pocket_casts.svg" alt="pocket casts"></a>
            <a href="https://soundcloud.com" target="_blank" class="details__social-item"><img src="../assets/images/icons/soundcloud.svg" alt="soundcloud"></a>
            <a href="https://podcasts.apple.com" target="_blank" class="details__social-item"><img src="../assets/images/icons/apple_podcasts.svg" alt="apple podcasts"></a>
            <a href="https://overcast.fm" target="_blank" class="details__social-item"><img src="../assets/images/icons/overcast.svg" alt="overcast"></a>
          </div>
        <div class="rating__wrapper">
          <img v-for="i in sourceData.desc.rating" :key="i" src="../assets/images/icons/star.svg" alt="">
        </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import data from "../data";
import {useRoute} from "vue-router"
import {computed} from "vue";

const route = useRoute()

let episodeId = computed(() => {
  return parseInt(route.params.id)
})

let sourceData = computed(() => {
  return data.episodesData.find(episodeData => episodeData.id === episodeId.value)
})

let image = new URL(sourceData.value.image, import.meta.url).href

</script>
