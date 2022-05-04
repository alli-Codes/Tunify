<template>
	
	<Category :type="type"></Category>
	<div id="song__section">

		<div id="container">
			<Song  v-for="(song, key) in songData" :key="key" :title="song.title" :artist="song.artist" />
			
		</div>
	</div>

</template>

<script>
	import Song from './Song'
	import Category from './Category'

	export default{
		name: 'Songs',

		components: {
			Song,
			Category
		},

		data() {
			return{
				type: 'Trending Songs',
				songData: [
					{title: 'Call Me', artist: 'Joeboy'},
					{title: 'Call Me', artist: 'Joeboy'},
					{title: 'Call Me', artist: 'Joeboy'},
					{title: 'Call Me', artist: 'Joeboy'},
					{title: 'Call Me', artist: 'Joeboy'},
				]
			}
		}
	}
</script>

<style scoped>
	
	#song__section{
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