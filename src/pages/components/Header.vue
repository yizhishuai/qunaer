<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe667;</span></div>
    <div class="header-input"><span class="iconfont">&#xe618;</span></div>
    <div class="header-right">{{this.city}}<span class="iconfont">&#xe6aa;</span></div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props:{
    city: String
  }
}
</script>

<style scoped>
.header
    {
    display: flex;
    line-height:.86rem;
    background:#00bcd4;
    color: #fff;
    }
    .header-left
      {
      width: .64rem;
      float: left;
      padding-left:0.1rem;
      }
      .back-icon
        {
        text-align: center;
        font-size: .4rem;
        }
    .header-input
      {
      flex: 1;
      height: .64rem;
      line-height: .64rem;
      margin-top: .12rem;
      margin-left: .2rem;
      padding-left: .2rem;
      background: #fff;
      border-radius: .1rem;
      color: #ccc;
      }
    .header-right
      {
      min-width: 1.04rem;
      padding: 0 .1rem;
      float: right;
      text-align: center;
      color: #fff;
      }
      .arrow-icon
        {
        margin-left: -.04rem;
        font-size: .24rem;
        }
	</style>
