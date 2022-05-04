<template>

  <div id="container">
    <Header></Header>
    <Songs></Songs>
    <Albums></Albums>
  </div>

</template>

<script>
import Header from './components/Header'
import Songs from './components/Songs/Songs'
import Albums from './components/Albums/Albums'

export default {
  name: 'App',

  components: {
    Header,
    Songs,
    Albums
  },
}
</script>

<style>
  
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

#app {
  font-family: lato, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

</style>
