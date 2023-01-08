<template>
  <section class="newsletter section">
    <div class="container">
      <div class="newsletter__wrapper">
        <div class="newsletter__text">
          <h2 class="section__subtitle">Email Newsletter</h2>
          <h3 class="section__title">Subscribe for updates</h3>
        </div>
        <form @submit.prevent class="newsletter__form">
          <input type="text" class="form__input" placeholder="Name">
          <input type="text" class="form__input" placeholder="Email">
          <input type="submit" class="form__submit btn" value="Submit">
        </form>
      </div>
    </div>
  </section>
</template>

<script>

</script>

<style scoped>

</style>