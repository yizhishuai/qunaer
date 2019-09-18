<template>
	<div class="header">
		<router-link to="/">
		<span class="iconfont">&#xe667;</span>
	    </router-link>
		国内城市
	</div>
</template>
<script>
export default{
	name:'CityHeader'
}	
</script>
<style scoped>
	.header{
		position: relative;
		height:.86rem;
		line-height: .86rem;
		background-color: #00bcd4;
		font-family: 0.4rem;
		text-align: center;
		color:#fff;
	}
	.iconfont
	{
		width: .5rem;
		position: absolute;
		text-align: center;
		top:0;
		left:0;
		color:#fff;
	}
</style>