<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" />
      <div class="banner-info">
        <div class="icon-num">
          <div class="banner-number">
            <span class="iconfont banner-icon">&#xe61b;</span>
            {{this.gallaryImgs.length}}
          </div>
        </div>
        <div class="banner-title">{{this.sightName}}</div>
      </div>
    </div>
    <common-gallary :imgs="gallaryImgs" v-show="showGallary" @close="handleClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleClose () {
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
