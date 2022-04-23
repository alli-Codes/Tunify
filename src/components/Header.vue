<template>
	
	<div id="header">
		<div id="logo__section">
			<button id="drop__btn" class="fas fa-bars"></button>
			<h3>Tunify</h3>
		</div>

		<div id="search__section">
			<div id="search__icon"></div>
			<input type="search" id="search__input" placeholder="Search for songs">
		</div>

		<div id="user__section">
			<button id="user__notification" class="fas fa-bell"></button>
			<button id="user__settings" class="fas fa-cog"></button>
			<div id="user__info">
				<div id="user__icon"></div>
				<p id="user__name"></p>
				<button id="user__options" class="fas fa-angle-down"></button>
			</div>
		</div>
	</div>

</template>

<script>
	
	export default{
		name: 'Header',
	}

</script>

<style scoped>
	
	#header{
		background-color: green;
		height: 5rem;
		width: 100%;
		display: flex;

	}

	#logo__section h3{
		color: #00D38B;
	}

</style>