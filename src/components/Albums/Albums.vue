<template>
	
	<Category :type="type" />
	<div id="album__section">

		<div id="container">
			<Song v-for="(song, key) in songData" :key="key" :title="song.title" :artist="song.artist" />
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