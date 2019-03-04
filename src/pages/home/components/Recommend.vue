<template>
  <div>
    <div class="title">
      <span class="iconfont icon-background">&#xe757;</span>
      猜你喜欢
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg',
        title: '长隆野生动物世界',
        comment: '95240',
        price: '208.9',
        place: '广州长隆...'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg',
        title: '长隆欢乐世界',
        comment: '51080',
        price: '174',
        place: '广州长隆...'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/1faf03354267996c8b039aa15290377b.jpg_200x200_7d3389d4.jpg',
        title: '天适樱花悠乐园',
        comment: '1262',
        price: '48',
        place: '从化市'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/27/ef08b0cb4a5afb2f570e5c4dff5f743e.jpg_200x200_f3ad8918.jpg',
        title: '长隆国际大马戏院',
        comment: '46979',
        price: '69.7',
        place: '番禺'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/20/41d723daadc98045fe6b7283ba0af40c.jpg_200x200_5a05d5bc.jpg',
        title: '碧水湾温泉度假村',
        comment: '1972',
        price: '95',
        place: '从化市'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/31/74eabd4dc95afd494d92a5006c9ad4f5.water.jpg_200x200_b27fe752.jpg',
        title: '美林湖温泉',
        comment: '1736',
        price: '78',
        place: '花都区'
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1601/3d/3dc7f222d6bca6a790.img.jpg_200x200_e0bb3017.jpg',
        title: '广州花城汇MAG环球魔幻世界',
        comment: '4290',
        price: '126.9',
        place: '广州'
      }]
    }
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
