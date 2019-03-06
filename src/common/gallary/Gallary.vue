<template>
  <div class="container" @click="handleGallaryClick">
    <div class="wrapper">
      <swiper :options="SwiperOptions">
        <swiper-slide v-for="(item,index) in imgs" :key="index">
          <img class="gallary-img" :src="item"/>
        </swiper-slide>
        <!--定义播图下面的白点-->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      SwiperOptions: {
        pagination: '.swiper-pagination', // 白点
        paginationType: 'fraction', // 轮播图下面的数字
        observeParents: true, // 自动刷新轮播图
        observer: true// 自动刷新轮播图
      }
    }
  },
  methods: {
    handleGallaryClick () {
      this.$emit('close')
    }
  }
}

</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow: inherit
  .container
    display: flex
    flex-direction: column
    justify-content: center
    z-index: 99
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    .wrapper
      width: 100%
      height: 0
      padding-bottom: 100%
      .gallary-img
        width: 100%
        height 100%
      .swiper-pagination
        color: #fff
        bottom: -4rem
</style>
