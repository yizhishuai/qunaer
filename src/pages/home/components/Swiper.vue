<template>
	<div id="swiper">
	<swiper :options="swiperOption" v-if="list.length">
    <swiper-slide  v-for="item in list" :key="item.id"><img class="img-swiper" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
</template>
<script>
export default{
	name:'HomeSwiper',
  props:{
    list:Array
  },
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
<style  scoped>
#swiper
  {
  overflow:hidden;
  width:100%;
  }
  .img-swiper
    {
   width:100%;
	 overflow:hidden;
    }
</style>