<template>
	
	<div id="song__container">
		<div id="song__image">
			<img src="../../assets/images/rema2.jpg" alt="">
		</div>
		<div id="song__description">
			<h5 id="song__title">{{artist}}</h5>
			<p id="song__artist">{{follows}}</p>
		</div>
	</div>

</template>

<script>
	
	export default {
		name: 'Artist',
		props: ['follows', 'artist'],
	}

</script>

<style scoped>
	
	#song__container{
		/*background-color: blue;*/
		height: 10rem;
		width: 6rem;
		margin: 0 2rem 0 0;
		display: flex;
		flex-direction: column;
		justify-content: space-evenly;
	}

	#song__index{
		background-color: white;
		height: 1rem;
		width: 1rem;
		border-top-left-radius: 5px;
		border-top-right-radius: 5px;
		font-size: 7px;
		display: flex;
		align-items: center;
		justify-content: center;
		position: absolute;
		top: 0;
		left: 5rem;
	}

	#song__image{
		/*background-color: red;*/
		height: 6rem;
		width: 100%;
		position: relative;
	}

	#song__image img{
		height: 100%;
		/*width: 100%;*/
		border-radius: 100%;

	}

	#song__description{
		/*background-color: red;*/
		font-size: 12px;
	}

	#song__title{
		color: #00D38B;
	}

	#song__artist{
		color: rgba(0, 0, 0, 0.4);
		font-size: 10px;
		font-weight: bold;
	}

</style>