<template>
	
	<Category :type="type" />
	<div id="album__section">

		<div id="container">
			<Song v-for="(song, index) in songData" 
			:key="index" 
			:index="index" 
			:title="song.title" 
			:artist="song.artist" 
			:image="song.image"
		/>

		</div>
	</div>

</template>

<script>
	import Song from '../Songs/Song'
	import Category from '../Songs/Category'

	export default{
		name: 'Albums',
		components: {
			Song,
			Category
		},
		data() {
			return{
				type: 'Trending Albums',
				songData: [
					{title: 'Calm Down', artist: 'Rema', image: '../images/rema2.jpg'},
					{title: 'Heavens Gate', artist: 'Burna Boy', image: '../images/burnaboy.jpg'},
					{title: 'Call Me', artist: 'Joeboy', image: '../images/Joeboy.jpg'},
					{title: 'Weekend', artist: 'Patoranking', image: '../images/patoranking.jpg'},
					{title: 'Davido', artist: 'Jowo', image: '../images/davido.jpg'},
				]
			}
		}
	}
</script>

<style scoped>
	
	#album__section{
		/*background-color: green;*/
		width: 100%;
		overflow-x: scroll;
	}

	#container{
		/*background-color: pink;*/
		padding: 0 1rem;
		display: inline-flex;
		overflow-x: scroll;
	}

</style>