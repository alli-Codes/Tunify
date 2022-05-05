<template>
	
	<Category :type="type" />
	<div id="artist__section">

		<div id="container">
			<Artist v-for="(data, index) in songData" :key="index" :artist="data.artist" :follows="data.follows" />
		</div>
	</div>

</template>

<script>
	import Artist from './Artist'
	import Category from '../Songs/Category'

	export default{
		name: 'Artists',
		components: {
			Artist,
			Category
		},
		data() {
			return{
				type: 'Popular Artists',
				songData: [
					{follows: 'Call Me', artist: 'Joeboy'},
					{follows: 'Call Me', artist: 'Joeboy'},
					{follows: 'Call Me', artist: 'Joeboy'},
					{follows: 'Call Me', artist: 'Joeboy'},
					{follows: 'Call Me', artist: 'Joeboy'},
				]
			}
		}
	}
</script>

<style scoped>
	
	#artist__section{
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