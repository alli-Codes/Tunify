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

    components: {
      Songs, Albums, Artists, Radios
    }
  }
  
</script>

<style>
  #explore{
    margin: 1rem 0 0 0;
  }

  @media (min-width: 500px){
    #explore{
      background-color: #FAFAFA;
      margin-left: 13rem;
    }
  }
</style>