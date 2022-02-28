<template>
  <nuxt-link :to="'jokes/' + id">
  <div class='joke'>
      <p> {{ joke }}</p>
  </div>
  </nuxt-link>
</template>

<script>
export default {
    name: 'Joke',
    props: ['joke', 'id']
}
</script>

<style>
    .joke {
        border-bottom: 1px solid black;
        margin: 10px;
    }
</style>