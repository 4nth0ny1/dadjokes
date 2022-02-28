<template>
  <header class="header">
      <h1 class="title">Dad Jokes</h1>
      <ul>
          <li>
            <nuxt-link to='/'>Home</nuxt-link>
          </li>
          <li>
            <nuxt-link to='/about'>About</nuxt-link>
          </li>
          <li>
            <nuxt-link to='/jokes'>Jokes</nuxt-link>
          </li>
      </ul>
  </header>
</template>

<script>
export default {
    name: 'AppHeader'
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border-bottom: 1px solid black;
    background: linear-gradient(180deg, rgba(233,242,244,1) 0%, rgba(0,159,230,1) 100%);
    padding: 10px;
  }

  ul {
    display: flex;
    flex-direction: row;
  }

  li {
    margin: 10px;
    list-style: none;
    color: black;
    text-decoration: none;
  }
</style>