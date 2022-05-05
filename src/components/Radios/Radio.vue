<template>
	
	<div id="radio__container">
		<div id="radio__image">
			<img :src="image" alt="">
		</div>
		<div id="radio__description">
			<h5 id="radio__title">{{artist}}</h5>
			<p id="radio__artist">{{follows}}</p>
		</div>
	</div>

</template>

<script>
	
	export default {
		name: 'Radio',
		props: ['follows', 'artist', 'image'],
	}

</script>

<style scoped>
	
	#radio__container{
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

	#radio__image{
		/*background-color: red;*/
		height: 6rem;
		width: 100%;
		position: relative;
	}

	#radio__image img{
		height: 100%;
		width: 100%;
		border-radius: 100%;
		object-fit: cover;		
	}

	#radio__description{
		/*background-color: red;*/
		font-size: 12px;
	}

	#radio__title{
		/*color: #00D38B;*/
	}

	#radio__artist{
		color: rgba(0, 0, 0, 0.4);
		font-size: 10px;
		font-weight: bold;
	}

</style>