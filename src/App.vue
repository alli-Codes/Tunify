<template>

  <div id="container">
    <Header></Header>
  </div>

</template>

<script>
import Header from './components/Header'
// import {greeting} from './message.js'

export default {
  name: 'App',

  components: {
    Header
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

</style>
