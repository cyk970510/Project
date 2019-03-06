<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_600x330_b5e86902.jpg"/>
      <div class="banner-info">
        <div class="banner-title">长隆野生动物世界(AAAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe636;</span>
          102
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1412/66/cd09ac9548221dcc4cef8dde5913c780.water.jpg_r_800x800_bea4d4a4.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      bottom: 0
      right: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        font-size: .32rem
        padding: 0 .2rem
        flex: 1
      .banner-number
        margin-top .18rem
        padding: 0 .4rem
        height: .32rem
        line-height: .32rem
        border-radius: .2rem
        font-size .26rem
        background: rgbs(0, 0, 0, .8)
        .banner-icon
          font-size .26rem
</style>
