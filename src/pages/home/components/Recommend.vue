<template>
  <div>
    <div class="title">
      <span class="iconfont icon-background">&#xe757;</span>
      猜你喜欢
    </div>
    <ul>
        <router-link tag="li"
                     class="item border-bottom"
                     v-for="item of recommendList"
                     :key="item.id"
                     :to="'/detail/' + item.id"
                     @click="scrollTop()"
        >
          <img class="item-img" :src="item.imgUrl" />
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <div class="item-comment">
              <span class="iconfont item-comment-icon">&#xe600;</span>
              <span class="item-comment-number">{{item.comment}}条评论</span>
            </div>
            <div class="item-price">
              <span class="item-price-icon">¥<em class="item-price-money">{{item.price}}</em></span>
              起
              <span class="item-price-place">{{item.place}}</span>
            </div>
          </div>
        </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    .icon-background
      color: red
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipse()
      .item-comment
        line-height: .4rem
        .item-comment-icon
          color: #ffb436
          font-size: .22rem
        .item-comment-number
          font-size: .24rem
          padding: .4rem
      .item-price
        line-height: .44rem
        margin-top: .16rem
        font-size: .24rem
        .item-price-icon
          color: #ff8300
          .item-price-money
            font-size: .4rem
        .item-price-place
          float: right
</style>
