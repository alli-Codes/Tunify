<template>
	
	<div id="sidebar">
		
		<div id="browse__section">
			<label for="Browse">Browse</label>
			<div id="browse__items">
				<div id="browse__item">
					<i class="fas fa-home"></i><p>Home</p>
				</div>

				<div id="browse__item">
					<i class="fas fa-compass"></i><p>Explore</p>
				</div>

				<div id="browse__item">
					<i class="fas fa-headphones"></i><p>Songs</p>
				</div>

				<div id="browse__item">
					<i class="fas fa-user"></i><p>Artists</p>
				</div>

				<div id="browse__item">
					<i class="fas fa-record-vinyl"></i><p>Albums</p>
				</div>

				<div id="browse__item">
					<i class="fas fa-satellite-dish"></i><p>Radio</p>
				</div>
			</div>
		</div>

		<div id="library__section">
			<label for="library">Your Library</label>
			<div id="library__items">
				<div id="library__item">
					<i class="fas fa-clock"></i><p>Recently Played</p>
				</div>

				<div id="library__item">
					<i class="fas fa-heart"></i><p>Favorites</p>
				</div>

				<div id="library__item">
					<i class="fas fa-record-vinyl"></i><p>Playlists</p>
				</div>

			</div>
		</div>

		<div id="store__section">
				
				<div id="google__card">
					<i class="fab fa-apple"></i>
					<div id="google__text">
						<p>Download on the</p>
						<h5>App Store</h5>
					</div>
				</div>

				<div id="google__card">
					<i class="fab fa-google-play"></i>
					<div id="google__text">
						<p>GET IT ON</p>
						<h5>Google Play</h5>
					</div>
				</div>


		</div>

	</div>

</template>

<script>
	
	export default {
		name: 'Sidebar',

	}

</script>

<style scoped>
	
	#sidebar{
		background-color: rgb(255, 250, 250);
		height: 100%;
		width: 13rem;
		/*padding: 1rem 0;*/
		position: fixed;
		z-index: 2000;
		overflow-y: auto;
		display: flex-block;
	}

	#browse__section, #library__section{
		/*background-color: pink;*/
		width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		align-items: stretch;
	}

	#browse__section label, #library__section label{
		color: rgb(160, 150, 150);
		padding: 2rem 0 1rem 1rem;
		font-size: 12px;
		align-self: flex-start;
	}

	#browse__item, #library__item{
		/*background-color: green;*/
		/*width: 100%;*/
		padding: .5rem 1rem;
		margin: .5rem 0;
		display: flex;
		font-size: 12px;
		font-weight: bold;
	}

	#browse__item:nth-child(2){
		color: #00D38B;
		background-image: linear-gradient(to top, rgba(255, 255, 255, 0.5), rgba(255, 255, 255, 0.7));
		border-left: .3rem solid #00D38B;
		padding-left: .7rem;
	}

	#browse__item p, #library__item p{
		margin: 0 0 0 1rem;
	}

	#store__section{
		padding: 0 0 0 1rem;
		margin-bottom: 7rem;
	}

	#google__card{
		height: 4rem;
		width: 70%;
		margin: 1.5rem 0;
		border: 2px solid black;
		border-radius: 5px;
		display: flex;
		justify-content: space-around;
		align-items: center;
	}

	#google__card i{
		font-size: 1.5rem;
	}

	#google__text{

	}

	#google__text p{
		font-size: 10px;
		text-align: left;
	}

	#google__text h5{
		font-weight: bold;
		font-size: 16px;
	}

</style>