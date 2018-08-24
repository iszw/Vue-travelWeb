<template>
  <div>
    <div class="recommend-title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
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
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
          title: '上海迪士尼乐园',
          desc: '探索令人难忘的六大主题园区、迪士尼小镇以及星愿公园等精彩目的地!'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
          title: '杭州极地海洋世界',
          desc: '模拟生态环境里与海洋动物的亲密接触'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/e6/e646f4221574cc2a90.water.jpg_200x200_d9b6cabd.jpg',
          title: '双溪竹海漂流',
          desc: '江南惊险漂流，水清、竹多、落差大'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1807/83/83d11e424ce11192a3.img.jpg_200x200_768d2d89.jpg',
          title: '杭州宋城',
          desc: '杭州宋城是中国大陆人气超旺的主题公园'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top .2rem
    line-height .6rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        margin-top .1rem
        line-height .3rem
        color #bbb
        ellipsis()
      .item-btn
        line-height .44rem
        background #FFB66A
        margin-top .2rem
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
