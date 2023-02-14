<template>
	<div id="top" class="container">
		<div class="first-cont">
			<p>
				LAST CHANCE! 5 days left to register for out 4-week Intro to UI Design & Figma Fundamentals course! <span>Sign up now!</span>
			</p>
		</div>
		<div class="second-cont">
			<div class="second-cont-1">
				<h3>Dribbble</h3>
				<p>Inspiration</p>
				<p>Find Work</p>
				<p>Learn Design</p>
				<p>Go Pro</p>
				<p>Hire Designers</p>
			</div>
			<div class="second-cont-2">
				<i id="i" class="fas regular fa-magnifying-glass"></i>
				<p class="p">Sign in</p>
				<p class="c-sign-up">Sign up</p>
			</div>
		</div>

	</div>
</template>
  
<script>
  export default {
	name: "HeaderPart"
}
</script>
  
<style scoped>

	.container{
		font-family: 'Roboto', sans-serif;
	}
  .first-cont{
	background-color: rgb(0, 0, 31);
	color: white;
	height: 7vh;
	display: flex;
	justify-content: center;
	font-size: 14px;
  }

  .first-cont p span{
	color: red;
  }

  .second-cont{
	display: flex;
	height: 12vh;
	background-color: white;
  }
  
  .second-cont-1{
	display: flex;
	flex: 1;
	margin: 0 1vw;
	align-items: center;
	justify-content: space-around;
	color: rgb(121, 120, 120);
  }

  .second-cont-1 h3,p{
	cursor:pointer;
  }

  
  .second-cont-2{
	display: flex;
	align-items: center;
	/* margin-left: 38vw;  */
	justify-content: space-around;
  }

  .c-sign-up{
	margin-right: 2vw;
	color: white;
	padding: 1.5vh 1.5vw;
	background-color: rgb(197, 74, 53);
	border-radius: 8px;
	cursor:pointer;
  }

  .second-cont-2 .p,#i{
	margin-right: 2vw;
	color: rgb(121, 120, 120);
	cursor:pointer;
  }


</style>