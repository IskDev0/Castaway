<script setup>
import TheHeader from "./components/TheHeader.vue"
import TheFooter from "./components/TheFooter.vue";


</script>

<template>
  <TheHeader/>
  <main class="main">
    <RouterView/>
  </main>
  <TheFooter/>
</template>
