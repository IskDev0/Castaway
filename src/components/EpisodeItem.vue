<template>
  <div class="episode">
    <img class="episode__img" :src="image" alt="podcast image">
    <div class="episode__text">
      <p class="episode__genre">{{ episode.genre }}</p>
      <p class="section__subtitle episode__number">Episode {{ episode.id }}</p>
      <p class="section__title episode__title">{{ episode.title }}</p>
      <p class="desc episode__desc">{{ episode.body }}</p>
      <button @click="$router.push(`episodes/${episode.id}`)" class="episode__btn btn">View Episode Details</button>
    </div>
  </div>
</template>

<script setup>

let image = new URL(props.episode.image, import.meta.url).href

let props = defineProps({
  episode: {
    type: Object,
    required: true
  }
})

</script>
