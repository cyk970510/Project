<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  name: 'home',
  components: {
    HomeIcons: HomeIcons,
    HomeSwiper: HomeSwiper,
    HomeHeader: HomeHeader
  }
}
</script>

<style scoped>

</style>
