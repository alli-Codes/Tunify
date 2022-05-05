<template>
	
	<div id="container">
		<div id="title">
			<h4>{{type}}</h4>
		</div>

		<div id="type" v-show="isTrue">
			<p style="color: gray">Genre:</p>
			<div id="options">
				<p>Afrobeats</p>
				<i class="fas fa-angle-down"></i>
			</div>
		</div>
	</div>

</template>

<script>
	
	export default {
		name: 'Category',
		props: ['type', 'isTrue']

	}

</script>

<style scoped>
	
	#container{
		height: 2rem;
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		/*position: fixed;*/
	}

	#title h4{
		font-size: 13px;
	}

	#type{
		width: 6rem;
		font-size: 8px;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	#options{
		width: 4rem;
		display: flex;
		justify-content: space-evenly;
		align-items: center;
	}

	#options p{
		font-size: 10px;
	}



</style>