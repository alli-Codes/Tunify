<template>
  <div style="height: 100vh; width: 100%; background-color: rgba(0, 0, 0, 0.2); position: fixed; z-index: 1000;" v-show="isActive" @click="changeSlideState"></div>
	<div id="sidebar" :class="isActive ? 'slide__in' : '' ">
		
		<div id="browse__section">
			<label for="Browse">Browse</label>
			<div id="browse__items">
				<div id="browse__item">
					<i class="bx bx-home"></i><p>Home</p>
				</div>

				<div id="browse__item">
					<i class="bx bx-compass"></i><p>Explore</p>
				</div>

				<div id="browse__item">
					<i class="bx bx-headphone"></i><p>Songs</p>
				</div>

				<div id="browse__item">
					<i class="bx bx-user"></i><p>Artists</p>
				</div>

				<div id="browse__item">
					<i class="bx bx-album"></i><p>Albums</p>
				</div>

				<div id="browse__item">
					<i class="bx bx-radio"></i><p>Radio</p>
				</div>
			</div>
		</div>

		<div id="library__section">
			<label for="library">Your Library</label>
			<div id="library__items">
				<div id="library__item">
					<i class="bx bx-time"></i><p>Recently Played</p>
				</div>

				<div id="library__item">
					<i class="bx bx-heart"></i><p>Favorites</p>
				</div>

				<div id="library__item">
					<i class="bx bxs-playlist"></i><p>Playlists</p>
				</div>

			</div>
		</div>

		<div id="store__section">
				
				<div id="google__card">
					<i class="bx bxl-apple"></i>
					<div id="google__text">
						<p>Download on the</p>
						<h5>App Store</h5>
					</div>
				</div>

				<div id="google__card">
					<i class="bx bxl-play-store"></i>
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

    data(){
      return {
        slideIn: 'slide__in',
        slideOut: 'slide__out'
      }
    },

    props: {
      isActive: Boolean,
      changeSlideState: Function
    },

    methods: {
      
    },

	}

</script>

<style scoped>
	
	#sidebar{
		background-color: rgb(255, 250, 250);
		height: 100%;
		width: 13rem;
		/*padding: 1rem 0;*/
		position: fixed;
    transform: translateX(-100%);
    transition:.2s;
		z-index: 2000;
		overflow-y: auto;
		display: flex-block;
    box-shadow: 8px 11px 8px 0px #00000012;
	}

  @media (min-width: 500px){
    #sidebar{
      background-color: #FAFAFA;
      box-shadow: none;
      transform: translateX(0%);
/*       position: relative; */
    }
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
		background-image: linear-gradient(180deg, rgba(215, 252, 209, 0.05) 0%, rgba(255, 255, 255, 0) 100%), rgba(189, 189, 189, 0.05);
		border-left: .3rem solid #00D38B;
		padding-left: .7rem;
	}

  @media (min-width: 500px){
    #browse__item:nth-child(2){
      background-image: linear-gradient(180deg, rgba(215, 252, 209, 0.3), rgba(255, 255, 255, 0), rgba(196, 196, 196, 0.2));
    }
  }

	#browse__item p, #library__item p{
		margin: 0 0 0 1rem;
	}

	#store__section{
		padding: 0 0 0 1rem;
		margin-bottom: 7rem;
	}

	#google__card{
		height: 3.5rem;
		width: 65%;
		margin: 1.5rem 0;
		border: 2px solid black;
		border-radius: 5px;
		display: flex;
/* 		justify-content: space-around; */
		align-items: center;
	}

	#google__card i{
    margin: 0 .2rem;
		font-size: 1.7rem;
	}

	#google__text{
    text-align: left;
	}

	#google__text p{
		font-size: 10px;
/* 		text-align: left; */
	}

	#google__text h5{
		font-weight: bold;
		font-size: 12px;
	}

  /*Animation Here*/
  #sidebar.slide__in{
    transform: translateX(0);
  }


</style>