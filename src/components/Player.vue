<template>
	
	<div id="container">
		<div id="artist__details">
			<div id="artist__icon">
				<img src="../../public/images/rema2.jpg" alt="">
			</div>

			<div id="artist__description">
				<h5 id="artist__track">Calm Down</h5>
				<p id="artist__name">Rema</p>
			</div>
		</div>

		<div id="player__controls-parent">
			<div id="player__controls">
				<button id="prevBtn" class="bx bx-skip-previous"></button>
				<button id="playBtn"  class="bx bx-play-circle"></button>
				<button id="nextBtn" class="bx bx-skip-next"></button>
			</div>

			<div id="player__range">
				<p id="player__counter">0:00</p>
           <div class="slider__wrapper">
              <vue-slider />
           </div>   
				<p id="player__duration">3:01</p>
			</div>
		</div>

		<button id="minimizeBtn" class="bx bx-chevron-down"></button>
	</div>

</template>

<script>

  import VueSlider from 'vue-slider-component'
// you probably need to import built-in style
  import 'vue-slider-component/theme/antd.css'
	
	export default {
		name: 'Player',
    
    components: {
      VueSlider
    }
	}

</script>

<style scoped>
  
	#container{
		background-color: #E7E7E7;
		height: 4rem;
		width: 100%;
		padding: 0 1rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: fixed;
		bottom: 0;
		z-index: 1000;
    box-shadow: 4px -2px 14px 6px #284a3e0d;
	}

	#artist__details{
		flex: 1;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	#artist__icon{
		height: 1.5rem;
		width: 1.5rem;
		position: relative;
	}

	#artist__icon img{
		height: 100%;
		width: 100%;
		border-radius: 100%;
		object-fit: cover;
	}

	#artist__description{
		padding: .5rem;
		font-size: 10px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
	}

	#artist__description p{
		color: rgba(0, 0, 0, 0.4);
		/*font-weight: 500;*/
	}

	#player__controls-parent{
		flex: 5;
		display: flex;
		flex-direction: column-reverse;
		align-items: center;
		justify-content: space-around;

	}

	#player__controls{
    flex: .5;
		margin: 0 0 .2rem 0;
	}

	#player__controls button{
		background-color: transparent;
		color: #00D38B;
		margin: 0 .1rem;
		border: none;
		font-size: 1.5rem;
	}

	#prevBtn, #nextBtn{
		color: rgba(0, 0, 0, 0.5) !important;
	}

	#player__range{
		display: flex;
		align-items: center;
		font-size: 10px;
	}

  .vue-slider{
    width: 30vw !important;
    margin: 0 5px;
  }
  .slider__wrapper{
/*     padding: 0px .7em; */
  }

  #player__duration , #player__counter{
    padding: 0px .5em;
  }
  .labelActiveStyle {
    width: 30em;
  }

	#minimizeBtn{
    background-color: none;
		flex: .5;
		color: rgba(0, 0, 0, 0.3);
		border: none;
		font-size: 1rem;
	}

	@media (min-width: 402px) {
    #artist__icon{
      height: 2rem;
      width: 2rem;
    }
    
		#player__controls-parent{
			flex-direction: row;
		}

		#player__controls{
      flex: 1.5 !important;
			margin: 0;
		}

    #player__range{
/*       background: blue; */
      flex: 1;
    }

    .vue-slider{
      width: 25vw !important;
      margin: 0 5px;
    }
	}

  @media (min-width: 500px){
    #container{
      background-color: #F8F8F8;
      z-index: 2000;
    }
  }

</style>