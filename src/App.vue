<template>

  
  <div style="display: flex; flex-direction: column; align-items: center;">
    
    <div class="title">
      <h1>Fast Clicking Game</h1>
    </div>

    <div class="directions">

      <h4>Directions:</h4>
      <p>Click on the square immediately, to measure your clicking pace. Goodluck ;)</p>

    </div>

    <button id="play" @click="handlePlay" :disabled="isPlaying">Play</button>
  </div>

  <Block v-show="isPlaying" :delay="delay" />

</template>

<script>
import Block from './components/Block'
import {greeting} from './message.js'

export default {
  name: 'App',

  data() {
    return {
      isPlaying: false,
      delay: 3
    }
  },

  components: {
    Block
  },

  methods: {

    handlePlay() {
      this.isPlaying = true
      greeting()
      console.log(`It's playing`)
    },


  }
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
  padding: 5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.directions{
  height: 5rem;
  margin: 3rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
}

#play{
  color: white;
  background-color: rgb(20, 150, 90);
  padding: .5rem 2rem;
  border: none;
  border-radius: 5px;
}

#play:disabled{
  background-color: rgba(20, 150, 90, 0.6);
}

</style>
