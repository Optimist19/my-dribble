<template>
  <div class="flex-con">
	<div class="first-con">
		<h3>dribbble</h3>
		<p>
			Dribbble is the world's leading community<br>for creatives to share, grow,<br>and get hired
		</p>
		<div class="media">
			<a href="#"><i class="fa light fa-basketball"></i></a>
			<a href="#"><i class="fa-brands fa-twitter"></i></a>
			<a href="#"><i class="fa-brands fa-square-facebook"></i></a>
			<a href="#"><i class="fa-brands fa-instagram"></i></a>
			<a href="#"><i class="fa-brands fa-pinterest"></i></a>
		</div>
	</div>
	<div class="second-con">
		<p>For designers</p>
		<p>Go Pro!</p>
		<p>Explore design work</p>
		<p>Design blog</p>
		<p>Overtime podcast</p>
		<p>Playoffs</p>
		<p>weekly warm-Up</p>
		<p>Refer a Friend</p>
		<p>Code of conduct</p>
	</div>
	<div class="third-con">
		<p>Hire designers</p>
		<p>Post a job</p>
		<p>Post a freelance<br>project</p>
		<p>search for designers</p>
		<p>Brands</p>
		<p>Advertsie with us</p>
	</div>
	<div class="fourth-con">
		<p>Company</p>
		<p>About</p>
		<p>Careers</p>
		<p>Support</p>
		<p>Media kit</p>
		<p>Testimonials</p>
		<p>API</p>
		<p>Terms of service</p>
		<p>Privacy policy</p>
		<p>Cookie policy</p>
	</div>
	<div class="fifth-con">
		<p>Directives</p>
		<p>Design jobs</p>
		<p>Designers for hire</p>
		<p>Freelance designers for hire</p>
		<p>Tag</p>
		<p>Places</p>
		<p>Design assets</p>
		<p>Dribbble Marketplace</p>
		<p>Creative Market</p>
		<p>Fontspring</p>
		<p>Font Squirrel</p>
	</div>
	<div class="sixth-con">
		<p>Design Resources</p>
		<p>Freelancing</p>
		<p>Design Hiring</p>
		<p>Design Portfolio</p>
		<p>Design Education</p>
		<p>Creative Process</p>
		<p>Design Industry Trends</p>
	</div>
  </div>
</template>

<script>
export default {
	name: "FooterTB"
}
</script>

<style scoped>
	.flex-con{
		display: flex;
		justify-content: space-around;
		font-family: 'Roboto', sans-serif;
		font-size: 15px;
	}


	.flex-con .first-con p{
		margin-bottom: 4vh;
	}
	.flex-con .first-con .media a{
		color: black;
	}
	.flex-con .first-con .media a i{
		margin-right: 2vw;
	}

	.second-con p:first-child{
		font-weight: 700;
	}

	.flex-con .third-con p:first-child{
		font-weight: 700;
	}


	.flex-con .third-con p:nth-child(5){
		font-weight: 700;
	}

	.flex-con .fourth-con p:first-child{
		font-weight: 700;
	}

	.flex-con .fifth-con p:first-child{
		font-weight: 700;
	}


	.flex-con .fifth-con p:nth-child(7){
		font-weight: 700;
	}

	.flex-con .sixth-con p:first-child{
		font-weight: 700;
	}
</style>