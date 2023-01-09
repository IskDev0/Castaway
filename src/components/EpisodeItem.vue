<template>
  <div class="episode">
    <img :src="image" alt="podcast image">
    <div class="episode__text">
      <p class="episode__genre">{{ episode.genre }}</p>
      <p class="episode__number section__subtitle">Episode {{ episode.id }}</p>
      <p class="episode__title section__title">{{ episode.title }}</p>
      <p class="episode__desc desc">{{ episode.body }}</p>
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
