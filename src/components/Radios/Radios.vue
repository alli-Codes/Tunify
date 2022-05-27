<template>
	
	<Category :type="type"  :isTrue="isTrue"/>
	<div id="radio__section" class="scrollBar">

		<div id="container" class="scrollBar">
			<Radio v-for="(data, index) in songData" 
			:key="index" 
			:artist="data.artist" 
			:follows="data.follows" 
			:image="data.image"
		/>
		</div>
	</div>

</template>

<script>
	import Radio from './Radio'
	import Category from '../Songs/Category'

	export default{
		name: 'Radios',
		components: {
			Radio,
			Category
		},
		data() {
			return{
				type: 'Popular Radio Stations',
				isTrue: false,
				songData: [
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/patoranking.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/ruger.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/wizkid.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/coolfm.jpg'},
          {follows: 'Call Me', artist: 'Joeboy', image: '../images/patoranking.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/ruger.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/wizkid.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/coolfm.jpg'},
          {follows: 'Call Me', artist: 'Joeboy', image: '../images/ruger.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/Joeboy2.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/wizkid.jpg'},
					{follows: 'Call Me', artist: 'Joeboy', image: '../images/coolfm.jpg'},
				]
			}
		}
	}
</script>

<style scoped>
	
	#radio__section{
		width: 100%;
		margin-bottom: 1rem;
		overflow-x: scroll;
    text-align: left;
	}

	#container{
		padding: 0 1rem;
		display: inline-flex;
		overflow-x: scroll;
	}

</style>