<template>
	
	<Category :type="type"  :isTrue="isTrue"/>
	<div id="artist__section">

		<div id="container">
			<Artist v-for="(data, index) in songData" :key="index" :artist="data.artist" :follows="data.follows" />
		</div>
	</div>

</template>

<script>
	import Artist from './Radio'
	import Category from '../Songs/Category'

	export default{
		name: 'Radios',
		components: {
			Artist,
			Category
		},
		data() {
			return{
				type: 'Popular Radio Stations',
				isTrue: false,
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