<template>
	
	<div id="song__container">
		<div id="song__image">
			<div id="song__index">#{{key}}</div>
			<img src="../../assets/images/rema2.jpg" alt="">
		</div>
		<div id="song__description">
			<h5 id="song__title">{{title}}</h5>
			<p id="song__artist">{{artist}}</p>
		</div>
	</div>

</template>

<script>
	
	export default {
		name: 'Songs',
		props: ['key', 'title', 'artist'],
	}

</script>

<style scoped>
	
	#song__container{
		/*background-color: blue;*/
		height: 8rem;
		width: 5rem;
		margin: 0 1rem 0 0;
		display: flex;
		flex-direction: column;
		justify-content: space-evenly;
	}

	#song__index{
		background-color: white;
		height: 10px;
		width: 10px;
		border-top-left-radius: 10px;
		border-top-right-radius: 10px;
		position: absolute;
		top: 0;
		/*left: 100%;*/
	}

	#song__image{
		/*background-color: red;*/
		height: 5rem;
		width: 100%;
		position: relative;
	}

	#song__image img{
		height: 100%;
		/*width: 100%;*/
		border-radius: 5px;

	}

	#song__description{
		/*background-color: red;*/
		font-size: 12px;
	}

	#song__artist{
		color: rgba(0, 0, 0, 0.4);
		font-size: 10px;
		font-weight: bold;
	}

</style>