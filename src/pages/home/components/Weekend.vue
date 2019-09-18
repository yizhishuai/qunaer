<template>
	<div>
	 <div class="title">周末推荐</div>
     <div  class="item border-bottom" v-for="item of list">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
	</div>
</div>
</template>
<script>
export default{
  props:{
    list:Array
  },
	name:"HomeWeekend"
}	
</script>
<style scoped>
	.title
   {
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
   }
   .item{
    padding-top:0.1rem;
   }
   .item-img-wrapper{
    overflow: hidden;
    height:0;
    padding-bottom:37.09%;
   }
    .item-img{
      width: 100%;
      padding: 0 0.1rem 0.1rem 0;

    }
    .item-info
      {
      padding: .1rem;
      }
      .item-title
       {
       	line-height: .54rem;
        font-size: .32rem;
        /*ellipsis()*/
       }
      .item-desc
        {
        line-height: .4rem;
        color: #ccc;
      /*  ellipsis()*/
        }
</style>