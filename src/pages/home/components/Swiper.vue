<template>
  <div class="warpper">
    <swiper :options="swiperOption" v-if="ShowSwiper">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" >
      </swiper-slide>
      <!--定义播图下面的白点-->
      <div class="swiper-pagination"  slot="pagination"></div>
      <!--左右箭头-->
      <!--<div class="swiper-button-prev" slot="button-prev"></div>-->
      <!--<div class="swiper-button-next" slot="button-next"></div>-->
      <!--底部的滚动条-->
      <!--<div class="swiper-scrollbar"   slot="scrollbar"></div>-->
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', //  定义播图下面的白点
        loop: true,
        autoplay: 2000
      }
    }
  },
  computed: {
    ShowSwiper () {
      return this.swiperList.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .warpper >>> .swiper-pagination-bullet-active
    background: #fff
  .warpper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.26%
    background: #eee
    .swiper-img
      width: 100%
</style>
