<template>
	
	<div id="header">
		<div id="logo__section">
			<button id="drop__btn" class="bx bx-menu-alt-right"></button>
			<h3>Tunify</h3>
		</div>

		<div id="search__section">
			<div id="search__container">
				<i id="search__icon" class="bx bx-search"></i>
				<input type="search" id="search__input" placeholder="Search for songs,...">
			</div>
		</div>

		<div id="user__section">
			
			<button id="user__notification" class="bx bx-bell"><div id="notification__status"></div></button>
			<button id="user__settings" class="bx bx-cog"></button>
			<div id="user__info">
				<div id="user__details">
					<div id="user__icon"></div>
					<p id="user__name">Evans Allison</p>
				</div>
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
		background-color: white;
		height: 3.5rem;
		width: 100%;
		padding: 0 6px;
		margin: 0 0 1rem 0;
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: sticky;
		top: 0;
		z-index: 1000;
	}

	#logo__section{
		width: 5rem;
		display: flex;
		justify-content: space-around;
		/*align-items: center;*/
		/*background-color: red;*/
	}

	#logo__section h3{
		color: #00D38B;
		font-size: 15px;
	}

	button{
		background-color: transparent;
		color: rgba(0, 0, 0, 0.3);
		border: none;
	}

	#notification__status{
		background-color: #00D38B;
		height: .3rem;
		width: .3rem;
		border-radius: 100%;
		position: absolute;
		top: 1.2rem;
		left: 0.5rem;
	}

	#search__section {
		/*background-color: red;*/
		/*width: 90%;*/
		
	}

	#search__container{
		height: 2rem;
		width: 90%;
		/*border: 1px solid rgba(0, 0, 0, 0.3);*/
		border-radius: 5px;
		margin: 0 5px;
		display: flex;
		align-items: center;
	}

	#search__section i{
		color: rgba(0, 0, 0, 0.4);
		margin: 0 5px 0 7px;
		font-size: 12px;
		/*position: absolute;*/
	}

	#search__section input{
		height: 100%;
		width: 100%;
		border: none;
		outline: none;
		align-self: stretch;
		font-family: lato;
		font-size: 12px;
	}

	#search__section input::placeholder{
		color: rgba(0, 0, 0, 0.4);
	}

	#user__section{
		/*background-color: blue;*/
		width: 8rem;
		display: flex;
		justify-content: space-around;
		align-self: stretch;
	}

	#user__notification{
		position: relative;
	}

	#user__info{
		/*background-color: red;*/
		/*width: 40%;*/
		display: flex;
		justify-content: space-between;
		align-self: center;
	}

	#user__details{
		/*background-color: green;*/
		/*width: 5rem;*/
		display: flex;
		justify-content: center;
		align-items: center;
	}

	/*#user__details p{
		display: none;
	}*/

	#user__icon{
		background-image: url(../../public/images/user.jpg);
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
		height: 1rem;
		width: 1rem;
		margin-right: .5rem;
		border-radius: 100%;
	}

	#user__name {
		padding: 0 0 0 10px;
		display: none;
		font-size: 10px;
	}

	@media (min-width: 600px){
		#user__section{
			width: 15rem;
			align-self: stretch;
		}

		#user__section button{
			font-size: 1rem;
		}

		#search__section{
			width: 50%;
			justify-content: flex-start;
		}

		#search__container{
			/*background-color: green;*/
		}
	}

</style>