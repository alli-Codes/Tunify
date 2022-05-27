<template>
	
	<Category :type="type" :isTrue="isTrue" />
	<div id="artist__section" class="scrollBar">

		<div id="container" class="scrollBar">
			<Artist v-for="(data, index) in songData" 
			:key="index" 
			:artist="data.artist" 
			:follows="data.follows" 
			:image="data.image"
			/>
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
				isTrue: false,
				songData: [
					{follows: '23.8M Followers', artist: 'Davido', image: '../images/davido.jpg'},
					{follows: '14.4M Followers', artist: 'Wizkid', image: '../images/wizkid.jpg'},
					{follows: '10.1M Followers', artist: 'Burna Boy', image: '../images/burnaboy2.jpg'},
					{follows: '3.2M Followers', artist: 'Rema', image: '../images/rema3.jpg'},
					{follows: '2.1M Followers', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
          {follows: '23.8M Followers', artist: 'Davido', image: '../images/davido.jpg'},
					{follows: '14.4M Followers', artist: 'Wizkid', image: '../images/wizkid.jpg'},
					{follows: '10.1M Followers', artist: 'Burna Boy', image: '../images/burnaboy2.jpg'},
					{follows: '3.2M Followers', artist: 'Rema', image: '../images/rema3.jpg'},
					{follows: '2.1M Followers', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
          {follows: '14.4M Followers', artist: 'Wizkid', image: '../images/wizkid.jpg'},
					{follows: '10.1M Followers', artist: 'Burna Boy', image: '../images/burnaboy2.jpg'},
					{follows: '3.2M Followers', artist: 'Rema', image: '../images/rema3.jpg'},
					{follows: '2.1M Followers', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
				]
			}
		}
	}
</script>

<style scoped>
	
	#artist__section{
		width: 100%;
		margin-bottom: 1rem;
		overflow-x: scroll;
    text-align: left;
	}

	#container{
		/*background-color: pink;*/
		padding: 0 1rem;
		display: inline-flex;
		overflow-x: scroll;
	}

</style>