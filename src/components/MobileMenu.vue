<template>
  <div class="mobile">
  <nav class="mobile__menu">
    <a @click="$emit('close')" href="/" class="mobile__menu-link">Home</a>
    <a @click="$emit('close')" href="/#episodes" class="mobile__menu-link">Episodes</a>
    <a @click="$emit('close')" href="/#about" class="mobile__menu-link">About</a>
    <a @click="$emit('close')" href="/#footer" class="mobile__menu-link">Contact</a>
  </nav>
  </div>
</template>

<script setup>
</script>

