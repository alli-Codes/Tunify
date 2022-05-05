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
			<button id="playBtn"  class="fas fa-fast-play"></button>
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
		background-color: green;
		height: 4rem;
		width: 100%;
		display: flex;
		justify-content: space-around;
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

</style>