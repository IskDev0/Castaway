<template>
<section class="section reviews">
  <div class="container">
    <div class="reviews__wrapper">
      <div class="review" v-for="review in reviews" :key="review.id">
        <div class="score">
        <img v-for=" i in review.score" :key="i" src="../assets/images/icons/star.svg" alt="star"></div>
        <p class="review__text">{{review.text}}</p>
        <p class="review__author desc">{{review.author}}</p>
      </div>
    </div>
  </div>
</section>
</template>

<script setup>
import reviews from "../reviews";
</script>
