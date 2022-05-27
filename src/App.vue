<template>

  <div id="container">
    <Header :changeSlideState="changeSlideState" />
    <sidebar :isActive="isActive" :changeSlideState="changeSlideState" />
    <Player />
    <Explore />
  </div>

</template>

<script>
import Header from './components/Header'
import Sidebar from './components/Sidebar'
import Explore from './components/Explore-Page'
import Player from './components/Player'

export default {
  name: 'App',
  
  data(){
    return {    
      isActive: false,
    }
  },
  components: {
    Header,
    Sidebar,
    Explore,
    Player
  },

   methods: {
      changeSlideState() {
        !this.isActive ? this.isActive = true : this.isActive = false
      },

     exit(){
        this.isActive ? this.isActive = false : this.isActive = true
      }
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
  font-family: lato, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  margin: 0 0 5rem 0;
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vue-slider-process{
    background-color:#00D38B !important;
    
  }

  .vue-slider-rail{
    background: #00000024;
    height:0.2em;
  }

button{
  outline: none;
}

.scrollBar::-webkit-scrollbar {
  display: none;
}

</style>
