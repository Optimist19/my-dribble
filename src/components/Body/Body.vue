<template>
	<div class="container">
		<div class="container-vid">
			<video class="background-video" autoplay loop muted poster="../../assets/backgroundvid.mp4">
			<source src="../../assets/backgroundvid.mp4" type="video/mp4">
			</video>
			<div class="list">
				<p :class="{discover:true}">{{discover}}</p>
				<p class="list-p">Animation</p>
				<p class="list-p">Branding</p>
				<p class="list-p">Illustration</p>
				<p class="list-p">Mobile</p>
				<p class="list-p">Print</p>
				<p class="list-p">Product&nbsp;Design </p>
				<p class="list-p">Typography</p>
				<p class="list-p">Web&nbsp;Design</p>
			</div>
			<div class="center">
				<p class="f-p">Explore the world's leading<br>design portfolios</p>
				<p class="s-p">
					Millions of designers and agencies around the world showcase their portfolio work on<br>Dribbble - the home to the world's best design and creative professionals.
				</p>
				<i class="fas regular fa-magnifying-glass"></i>
				<input type="text">
				<div class="l-p">
					<span>Trending searches</span>
					<span>landing page</span>
					<span>ios</span>
					<span>food</span>
					<span>landingpage</span>
					<span>uxdesign</span>
					<span>app design</span>
				</div>
			</div>
			<p class="glebish">@glebich</p>
		</div>
		<BodyTwo />
		<BodyThree />
    </div>
</template>

<script>
import BodyTwo from "./BodyTwo.vue"
import BodyThree from "./BodyThree.vue"

export default {
	name: "BodyPart",
	data(){
		return{
			discover: "Discover",
			color: true
		}
	},
	
	components:{
		BodyTwo,
		BodyThree
	}
}
</script>

<style scoped>

	.container{
		font-family: 'Roboto', sans-serif;
	}

	.container .container-vid{
		height: 75vh;
	}


	.background-video {
		width: 100vw;
		height: 95vh;
		object-fit: cover;
		position: absolute;
		left: 0;
		right: 0;
		top: 0;
		bottom: 0;
		z-index: -1;
	}

	.container-vid .list{
		display: flex;
		color: white;
		justify-content: space-around;
		margin: 2.5vh 7vw;
		/* width: 90vw */
	}

	.container-vid .list .list-p{
		padding: 3vh 2vw;
		background-color: rgba(0, 0, 0, 0.5);
		border-radius: 20px;
		transition: background-color 0.2s ease-in;
		cursor: pointer;
		font-size: 16px;
	}

	.container-vid .list .list-p:hover{
		background-color: white;
		color: rgba(0, 0, 0, 0.5);
	}

	.container-vid .list .discover{
		background-color: white;
		color: rgba(0, 0, 0, 0.5);
		padding: 3vh 2vw;
		border-radius: 20px;
		font-size: 16px;
	}

	/* .container .list p:first-child {
		background-color: white;
		color: rgba(0, 0, 0, 0.5);
	} */
	.center{
		text-align: center;
	}

	.center .f-p{
		font-size: 35px;
		font-weight: bold;
	}
	
	
	.center .s-p{
		font-size: 20px;
	}

	.center .l-p{
		display: flex;
		margin-top: 2vh;
		margin-left: 22vw;
	}

	.center .l-p span{
		border-radius: 20px;
		padding: 1vh 1vw;
		background-color: rgba(0, 0, 0, 0.5);
		color: white;
		margin-right: 1vw;
		cursor: pointer;
		font-size: 14px;
	}

	



	.center input{
		position: relative;
		padding: 3vh 13vw;
		border-radius: 20px;
		border: none;
	}

	.center i{
		position: absolute;
		left: 33vw;
		z-index: 1;
		padding-top: 3vh;
		color: rgb(121, 120, 120);
	}

	.container-vid .glebish{
		float: right;
		margin-right: 3vw
	}
</style>