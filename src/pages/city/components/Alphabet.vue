<template>
	<div class="alphabet">
		<div class="alphabet-item" v-for="(item,key) of cities" :key="key"
		@click="handleLetterClick">{{key}}</div>
	</div>
</template>
<script>
export default{
	name:'CityAlphabet',
	props:{
		cities:Object
	},
	methods:{
		handleLetterClick(e){
			this.$emit('change',e.target.innerText)
		}
	}
}	
</script>
<style scoped>
.alphabet{
	display: flex;
	flex-direction: column;
	justify-content: center;
	position: fixed;
	top:1.6rem;
	right:0;
	bottom: 0;
	width: 0.4rem;
}
.alphabet-item{
	line-height: .4rem;
	text-align: center;
	color:#00bcd4;
	font-size: 0.28rem;
}
</style>