<template>
	<div class="list" ref="wrapper">
	<div>
	<div class="area">
		<div class="title border-topbuttom">您的位置</div>
		<div class="button-list">
			<div class="button-wrapper">
				<div class="button">北京市</div>
			</div>
		</div>	
	</div>
	<div class="area">
		<div class="title border-topbuttom">热门城市</div>
		<div class="button-list">
			<div class="button-wrapper" 
			v-for="item in hotCities">
				<div class="button">{{item.name}}</div>
			</div>
		</div>		
	</div>
	<div class="area" 
	 v-for="(item,key) of cities"
	 :key="key"
	 :ref="key">
		<div class="title border-topbuttom">{{key}}</div>	
		<div class="item">
		<div 
		class="item border-bottom"
		v-for="innerItem of item"
		:key="innerItem.id">{{innerItem.name}}</div>	
	</div>
	
	</div>
</div>
</div>
</template>
<script>
import BScroll from 'better-scroll'
export default{
	name:"CityList",
	props:{
		hotCities:Array,
		cities:Object,
		letter:String
	},
	mounted(){
		this.scroll = new BScroll(this.$refs.wrapper)
	},
	watch:{
		letter(){
			if(this.letter){
				const element = this.$refs[this.letter][0]
				this.scroll.scrollToElement(element)
				console.log(this.letter)
			}
		}
	}
}
</script>
<style scoped>
	.border-topbottom::before
      {
      	border-color: #ccc;
      }
   .border-topbottom::after
      {
      	border-color: #ccc;
      }
  .border-bottom::before
      {
      	border-color: #ccc;
      }
	.list{
	overflow: hidden;
    left: 0;
    right: 0;
    bottom: 0;
	}
	.title{
	line-height: .54rem;
	background: #eee;
	padding-left: .2rem;
	color: #666;
	font-size: .26rem;
	}
	.button-list{
		padding: .1rem .6rem .1rem .1rem;
		overflow: hidden;
	}
	  .button-wrapper{
		float:left;
		width: 33.3%;
	  }
	  .button{
		margin: .1rem;
		padding: .1rem 0;
		text-align: center;
		border:0.02rem solid #ccc;
		border-radius: 0.06rem;
	  }
	  .item
        {
        line-height: .76rem;
        padding-left: .2rem;
        }
</style>