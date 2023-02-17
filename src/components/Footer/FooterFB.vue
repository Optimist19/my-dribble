<template>
	<div class="fb">
		<!-- <span v-html="c"></span> -->
		<span>&copy;</span>
		<!-- <span>{{ c }}</span> -->
		<span>{{ year }}</span>
		<span>{{ copyRight }}</span>
		<span>{{ number }}</span>
		<a href="#"><i class="fa light fa-basketball"></i></a>
		
	</div>
</template>

<script>
// import {reactive, toRefs} from "vue"
	export default{
		name: "FooterFB",
		data(){
			return{
				// c: "&copy;",
				// c: "<p>&copy;</p>",
				year: "2023 Dribbble.",
				copyRight: "All rights reserved.",
				number: "20,677,342"
			}
		},
		// setup(){
		// 	const data = reactive({
		// 		c: "<sub>&copy;</sub>",
		// 		year: 2023,
		// 		copyRight: "All rights reserved",
		// 		number: "20,677,342"
		// 	})

		// 	return toRefs(...data)
			
		// }

	}

</script>

<style scoped>
	.fb{
		margin-left: 4vw;
	}

	.fb span:nth-child(2){
		margin-right: 0.2vw;
	}
	
	.fb span:nth-child(4){
		margin-left: 65vw;
	}
	
	.fb a i{
		font-size: 24px;
		margin-left: 0.5vw;
		color:rgb(255, 29, 29);
	}
</style>