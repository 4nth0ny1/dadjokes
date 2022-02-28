<template>
  <div class="jokes">
      <h1>All Jokes</h1>
      <SearchJokes class="search-bar" v-on:search-text="searchText"/>
      <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>

<script>
import axios from 'axios'
import Joke from '../../components/Joke.vue'
import SearchJokes from '../../components/SearchJokes.vue'

export default {
  components: {
    Joke, 
    SearchJokes
  },
  data() {
    return {
      jokes: []
    }
  },
  async created() {
    const config = {
      headers: {
        'Accept': 'application/json'
      }
    }
    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config);

      this.jokes = res.data.results

    } catch (error) {
      console.log(error)
    }
  },
  methods: {
    async searchText(text) {
      const config = {
        headers: {
          'Accept': 'application/json'
        }
      }
      try {
        const res = await axios.get(`https://icanhazdadjoke.com/search?term=${text}`, config);

        this.jokes = res.data.results

      } catch (error) {
        console.log(error)
      }
    }
  },
  head() {
      return {
          title: 'Dad jokes', 
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
  .jokes {
    width: 800px;
    margin: 0 auto;
    padding: 25px;
  }

  .jokes h1 {
    text-align: center;
  }

  .search-bar {
    text-align: center;
    margin: 20px 0;
  }

</style>