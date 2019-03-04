<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default {
  name: 'home',
  components: {
    HomeWeekend: HomeWeekend,
    HomeRecommend: HomeRecommend,
    HomeIcons: HomeIcons,
    HomeSwiper: HomeSwiper,
    HomeHeader: HomeHeader
  }
}
</script>

<style scoped>

</style>
