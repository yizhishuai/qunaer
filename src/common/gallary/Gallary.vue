<template>
	<div class="container" @click="handleContainerClick">
		<div class="wrapper" >
			<swiper :options="swiperOption">
    			<swiper-slide v-for='(item,index) in imgs' :key="index"><img class="swiper-img" :src="item">
    			</swiper-slide>
    		<div class="swiper-pagination"  slot="pagination"></div>
    		</swiper>
		</div>
	</div>
</template>
<script>
export default{
	name:'CommonGallary',
	props:{
	imgs:{
		type:Array,
		default () {
        return []
      }
    }
  },
	data(){
		return{
			con_style:{
				display:'none'
			},
			swiperOption:{
				pagination:'.swiper-pagination',
				paginationType:'fraction',
				observeParents:true,
				observer:true
			}
		}
	},
	methods:{
		handleContainerClick(){
			 this.$emit('close')
	}
  
  } 
}
</script>
<style scoped>
.container{
	display: flex;
	flex-direction: column;
	justify-content: center;
	z-index:99;
	position: fixed;
	left: 0;
	right: 0;
	top: 0;
	bottom: 0;
	background: #000;
}
.wrapper{
	height: 0;
	width: 100%;
	padding-bottom: 100%;
}
img{
	width: 100%; 
}
.swiper-pagination{
	color:#fff;
	bottom: -1rem;
}
.swiper-container{
	overflow: inherit;
}
</style>