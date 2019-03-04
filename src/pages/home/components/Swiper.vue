<template>
  <div class="warpper">
    <swiper :options="swiperOption">
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
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', //  定义播图下面的白点
        loop: true// 循环播图
      },
      swiperList: [{
        id: '001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/0a8f7c789d0e62966e2485d33bf7ebd3.jpg_750x200_b455610d.jpg'
      }, {
        id: '002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/892f011c3b7bd6815b460c659acc5651.jpg_750x200_e2242cfb.jpg'
      }, {
        id: '003',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/2e090c7af936930c119a28c2f62717f2.jpg_750x200_9fce1256.jpg'
      }, {
        id: '004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/5d157b6ab21b9f6606dd006765f84558.jpg_750x200_f93e4649.jpg'
      }]
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
