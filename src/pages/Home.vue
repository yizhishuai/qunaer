<template>
  <div class="hello">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from '@/pages/components/Header'
import HomeSwiper from '@/pages/components/Swiper'
import HomeIcons from '@/pages/components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
}
 </script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
