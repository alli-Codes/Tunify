<template>
  <div id="explore">
    <Songs />
    <Albums />
    <Artists />
    <Radios />
  </div>
</template>

<script>

  import Songs from './Songs/Songs'
  import Albums from './Albums/Albums'
  import Artists from './Artists/Artists'
  import Radios from './Radios/Radios'

  export default {
    name: 'Explore',

    data(){
      return{
        
      }
    },

    components: {
      Songs, Albums, Artists, Radios
    },

    methods: {
      
    }
  }
  
</script>

<style>
  #explore{
    background-color: #cdcdcd0a;
    height: 85vh;
    display: flex-block;
    padding: 1rem 0 0 0;
/*     margin: .5rem 0 0 0; */
    overflow-y: scroll;
  }

  #song__description{
		text-align: center;
	}

  @media (min-width: 500px){
    #explore{
      margin-left: 13rem;
    }
  }
</style>