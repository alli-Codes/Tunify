<template>

  <div id="container">
    <Header />
    <Player />
    <Songs />
    <Albums />
    <Artists />
    <Radios />
  </div>

</template>

<script>
import Header from './components/Header'
import Songs from './components/Songs/Songs'
import Albums from './components/Albums/Albums'
import Artists from './components/Artists/Artists'
import Radios from './components/Radios/Radios'
import Player from './components/Player'

export default {
  name: 'App',

  components: {
    Header,
    Songs,
    Albums,
    Artists,
    Radios,
    Player
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

  margin: 0 0 5rem 0;
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

button{
  outline: none;
}

</style>
