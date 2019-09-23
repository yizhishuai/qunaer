<template>
<div>
	<div class="header-abs" v-show="showAbs">
		<router-link tag='div' to='/' class="iconfont header-abs-back">&#xe667;</router-link>
	</div>
	<div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
		<router-link tag='div' to='/' class="iconfont  header-fixed-back">&#xe667;</router-link>
           经典详情
    </div>
</div>
</template>
<script>
export default{
	name:"DetailHeader",
	data(){
		return{
			showAbs:true,
			opacityStyle:{
				opacity:0
			}
		}
		
	},
	methods:{
		handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
	mounted(){
		window.addEventListener('scroll',this.handleScroll)
	}
}	
</script>
<style scoped>
.header-abs{
	position: absolute;
	left: .2rem;
	top: .2rem;
	width: .8rem;
	height: .8rem;
	border-radius: .4rem;
	line-height: .8rem;
	border-radius: .4rem;
    text-align: center;
	background:rgba(0,0,0,0.8);
}
.header-abs-back{
	color: #fff;
	font-size: .4rem;
}	
.header-fixed{
		z-index: 2;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		height:.86rem;
		line-height: .86rem;
		background-color: #00bcd4;
		font-family: 0.4rem;
		text-align: center;
		color:#fff;
	}
.header-fixed-back
     {
      position: absolute;
      top: 0;
      left: 0;
      width: .64rem;
      text-align: center;
      font-size: .4rem;
      color: #fff;
     }
	
</style>