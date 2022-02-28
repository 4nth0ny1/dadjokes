<template>
  <div class="about-container">
      <h1>About Dad Jokes</h1>
      <p>app that displays corny dad jokes</p>
  </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'About The App', 
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
    .about-container {
        width: 800px;
        margin: 0 auto;
        padding: 25px;
    }

    .about-container h1 {
        text-align: center;
    }
    
    .about-container p {
        text-align: center;
        margin: 20px 0;
    }

</style>