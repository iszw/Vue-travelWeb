<template>
  <div class="recommend">
    <div class="recommend-title">
      <span class="iconfont title-icon">&#xe69a;</span>
      <span class="title-text">热门推荐</span>
    </div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <div class="item-left">
          <span class="item-title">{{item.title}}</span>
          <span class="item-desc">{{item.desc}}</span>
          <div class="item-tags">
            <span class="item-tag" v-for="item in item.tags" :key="item.id">&nbsp;{{item}}&nbsp;</span>
          </div>
        </div>
        <div class="item-right">
          <strong class="item-price">¥{{item.price}}</strong>
          <button class="item-btn">预定</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'DatailRecommend',
  data () {
    return {
      recommendList: [
        {
          title: '【限量特惠】上海迪士尼儿童票',
          desc: '可订明日',
          tags: ['自营', '无需退票', '不可退'],
          price: '288'
        }, {
          title: '【夏末特惠】上海迪士尼乐园成人票',
          desc: '22:00前随买随用',
          tags: ['自营', '无需退票', '不可退'],
          price: '460'
        }, {
          title: '【限量特惠】上海迪士尼儿童票',
          desc: '可订明日',
          tags: ['条件退', '无购物', '已售4488'],
          price: '489'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .recommend
    width 100%
    .recommend-title
      line-height .8rem
      background #eee
      text-indent .2rem
      .title-icon
        color #fd6f71
        font-size .32rem
      .title-text
        margin-left .2rem
        font-size .32rem
        color #333
    .item
      display flex
      padding .2rem 0
      .item-left
        flex 2.92
        display flex
        flex-direction column
        justify-content center
        .item-title
          margin-right .1rem
          line-height .52rem
          padding 0
          font-size .3rem
        .item-desc
          display inline-block
          margin-left .2rem
          height .32rem
          color #616161
          font-size .24rem
          line-height .32rem
          white-space nowrap
        .item-tags
          display flex
          flex-direction row
          margin-left .2rem
          .item-tag
            display inline-block
            margin-top .08rem
            padding 0 .04rem
            height .32rem
            color #00afc7
            font-size .2rem
            line-height .32rem
            border .01rem solid #a5e4ec
            border-radius .08rem
      .item-right
        flex 1
        display flex
        flex-direction column
        justify-content center
        float right
        margin-right .3rem
        .item-price
          color #ff9800
          height .4rem
          text-align center
        .item-btn
          height .6rem
          color #fff
          font-size .28rem
          line-height .6rem
          border-radius .08rem
          background-image linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
</style>
