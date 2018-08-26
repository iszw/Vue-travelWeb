<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_600x330_8572a930.jpg" />
      <div class="banner-info">
        <div class="icon-num">
          <div class="banner-number">
            <span class="iconfont banner-icon">&#xe61b;</span>
            15
          </div>
        </div>
        <div class="banner-title">上海迪士尼乐园</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleColse"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_r_800x800_d6a63068.jpg', 'http://img1.qunarzz.com/sight/p0/1711/81/81ed632012f27eeaa3.img.jpg_r_800x800_93f1a7af.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleColse () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      position absolute
      left 0
      right 0
      bottom 0
      line-height .8rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .5))
      .banner-title
        font-size .36rem
        padding 0 .2rem
        color #fff
      .icon-num
        position relative
        padding 0 .2rem
        .banner-number
          height .4rem
          line-height .36rem
          width .8rem
          padding 0 .4rem
          border-radius .2rem
          background rgba(0, 0, 0, .5)
          font-size .24rem
          text-align center
          color #fff
          .banner-icon
            position relative
            top .04rem
</style>
