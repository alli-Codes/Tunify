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

		<div id="player__controls">
			<button id="prevBtn" class="fas fa-fast-backward"></button>
			<button id="playBtn"  class="fas fa-play-circle"></button>
			<button id="nextBtn" class="fas fa-fast-forward"></button>
		</div>

		<div id="player__range">
			<p id="player__counter">0:00</p>
			<input type="range">
			<p id="player__duration">3:01</p>
		</div>

		<button id="minimizeBtn" class="fas fa-arrow-alt-v"></button>
	</div>

</template>

<script>
	
	export default {
		name: 'Player'
	}

</script>

<style scoped>

	#container{
		background-color: white;
		height: 4rem;
		width: 100%;
		padding: 0 1rem;
		display: flex;
		justify-content: space-around;
		align-items: center;
		position: fixed;
		bottom: 0;
		z-index: 1000;
	}

	#artist__details{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	#artist__icon{
		height: 3rem;
		width: 3rem;
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
		font-size: 12px;
	}

	#artist__description p{
		color: rgba(0, 0, 0, 0.4);
		/*font-weight: 500;*/
	}

	#player__controls{

	}

	#player__controls button{
		background-color: transparent;
		color: #00D38B;
		margin: 0 .3rem;
		border: none;
		font-size: 1.2rem;
	}

	#prevBtn, #nextBtn{
		color: rgba(0, 0, 0, 0.5) !important;
	}

	#player__range{
		display: flex;
		align-items: center;
		font-size: 10px;
	}

	#player__range input{
		width: 6rem;
		margin: 0 .2rem;
	}


#player__range input[type='range'], #volume-input input[type='range'] {
    /*-webkit-appearance: none;*/
    background-color: transparent;
}

/*Chrome*/

#player__range input[type='range']::-webkit-slider-range-progress {
    -webkit-appearance: none;
    background-color: #00D38B;
    height: 20px;
}

#player__range input[type='range']::-webkit-slider-runnable-track, #volume-input input[type='range']::-webkit-slider-runnable-track {
    -webkit-appearance: none;
    /*background-color: #00D38B;*/
    background-color: rgba(255, 255, 255, 0.4);
    height: 2px;
}

#player__range input[type='range']::-webkit-slider-thumb{
    -webkit-appearance: none;

    background-color: red;
    /*background-color: #00D38B;*/
    height: 10px;
    width: 10px;
    border: 3px solid white;
    border-radius: 20px;

}

/** FF*/

#player__range input[type='range']::-moz-range-thumb, #volume-input input[type='range']::-moz-range-thumb {
    background-color: #00D38B;
    height: 10px;
    width: 10px;
    border: 3px solid white;
    border-radius: 20px;
}

#player__range input[type="range"]::-moz-range-progress, #volume-input input[type='range']::-moz-range-progress {
    background-color: #00D38B;
}

#player__range input[type="range"]::-moz-range-track, #volume-input input[type='range']::-moz-range-track {
    background-color: rgba(255, 255, 255, 0.4);
}

main::-moz-scrollbar-thumb {
  background-color: red;
}

</style>