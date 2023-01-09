<template>
  <header class="header">
    <div class="container">
      <div class="header__wrapper">
        <a href="" class="header__link">
          <img src="../assets/images/icons/logo.svg" alt="Logo" class="header__link-image">
        </a>
        <nav class="header__nav">
          <a href="/" class="header__nav-link">Home</a>
          <a href="/#episodes" class="header__nav-link">Episodes</a>
          <a href="/#about" class="header__nav-link">About</a>
          <a href="/#footer" class="header__nav-link">Contact</a>
        </nav>
        <div @click="openMobileMenu" class="openMobile"><div class="openMobile-line"></div></div>
      </div>
    </div>
    <MobileMenu @close="closeMobile" v-if="show" />
  </header>
</template>

<script setup>
import MobileMenu from "../components/MobileMenu.vue"

import {ref} from "vue";

let show = ref(false)

let closeMobile = () => {
  let btn = document.querySelector(".openMobile-line")
  btn.classList.remove("active")
  show.value = false
}

let openMobileMenu = () => {
  let btn = document.querySelector(".openMobile-line")
  btn.classList.toggle("active")
  show.value = !show.value
}


</script>

