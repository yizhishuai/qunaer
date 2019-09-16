<template>
	<div id="swiper">
	<swiper :options="swiperOption">
    <swiper-slide><img class="img-swiper" src="https://images.pexels.com/photos/2884462/pexels-photo-2884462.jpeg?auto=compress&cs=tinysrgb&dpr=2&w=500" ></swiper-slide>
    <swiper-slide><img class="img-swiper" src="https://images.pexels.com/photos/1438072/pexels-photo-1438072.jpeg?auto=compress&cs=tinysrgb&dpr=2&w=500"></swiper-slide>
    <swiper-slide><img class="img-swiper" src="https://images.pexels.com/photos/2884572/pexels-photo-2884572.jpeg?auto=compress&cs=tinysrgb&dpr=2&w=500"></swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
</template>
<script>
export default{
	name:'HomeSwiper',
	data(){
		return {
			swiperOption:{
		    pagination: '.swiper-pagination',
            loop:true
	      }
	      	
	   }
	}
}	
</script>
<<<<<<< HEAD
<style lang="stylus" scoped>
#swiper >>> .swiper-pagination-bullet-active
  background:#fff
#swiper
  overflow:hidden
  width:100%
  .img-swiper
    width:100%
    margin: -50px 0px -50px; 
	 overflow:hidden
=======
<style  scoped>
#swiper
  {
  overflow:hidden;
  width:100%;
  }
  .img-swiper
    {
    width:100%;
    margin: -50px 0px -50px; 
	overflow:hidden;
    }
>>>>>>> origin/swiper
</style>