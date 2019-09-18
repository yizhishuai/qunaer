<template>
	<div class="input">
		<input type="text" placeholder="输入城市名或拼音">
	</div>
</template>
<script>
export default{
	name:'CitySearch'
}	
</script>
<style scoped>
	.input{
		background-color: #00bcd4;
		height: 0.72rem;
		padding: 0 0.2rem;
	}
	input{
		text-align: center;
		height:0.62rem;
		width: 100%;
		border-radius: 0.6rem;
		padding: 0 0.1rem;
		box-sizing: border-box;
		color:#666;
	}
</style>