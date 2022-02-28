<template>
  <div class="home-container">
    <h1>best corny dad jokes on the web</h1>
  </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'Welcome to Dad Jokes', 
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Best place for corny dad jokes'
                }
            ]
        }
    }
}
</script>

<style>
    .home-container {
        width: 800px;
        margin: 0 auto;
        padding: 25px;
        text-align: center;
    }
</style>