
<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
          title: '杭州必游TOP10',
          desc: '杭州，前世今生与你有一场美丽的约会'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
          title: '承载杭城的历史之地',
          desc: '饱经沧桑的地方诉述这这座城的段段衷肠'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/bc/83feb2e003d0dd.jpg_r_640x214_0b7269b8.jpg',
          title: '杭州多样乐园',
          desc: '这个周末终于可以陪宝贝去玩耍啦'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ae/4fe23c6b6679e2.jpg_r_640x214_368a18d8.jpg',
          title: '美仑美奂的演出',
          desc: '一座有故事的城，天天有‘戏’在上演'
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
  .item-img-wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 37.1%
  .item-img
    width 100%
  .item-info
    padding-left .2rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #bbb
      ellipsis()
      padding-bottom .1rem
</style>
