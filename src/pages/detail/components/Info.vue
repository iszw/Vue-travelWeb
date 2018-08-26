<template>
  <div class="info border-bottom">
    <div class="info-content">
      <div class="score-content border-right">
        <div class="score-realcontent">
          <div class="score">
            <p class="score-score">5.0</p>
            <p class="score-text">分</p>
            <p class="score-desc">超赞</p>
          </div>
          <div class="comment">
            <p class="comment-comment">179754条评论</p>
            <p class="comment-raider">32条攻略</p>
          </div>
        </div>
        <div class="score-icon">
          <p class="iconfont">&#xe600;</p>
        </div>
      </div>
      <div class="intro-content">
        <div class="intro-realcontent">
          <div class="intro-desc">景点简介</div>
          <div class="intro-time">开放时间、贴士</div>
        </div>
        <div class="intro-icon">
          <p class="iconfont">&#xe600;</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DatailInfo'
}
</script>

<style lang="stylus" scoped>
  .info
    top -.1rem
    padding .2rem .2rem 0 .2rem
    margin-bottom .1rem
    background #fff
    border-radius .1rem .1rem 0 0
    .info-content
      display flex
      width 100%
      flex-direction row
      justify-content center
      .score-content
        position relative
        width 3.55rem
        display flex
        .score-realcontent
          flex 1
          .score
            display flex
            .score-score
              font-size .44rem
              color #ff8300;
              line-height .44rem
            .score-text
              font-size .28rem
              color #ff8300
              line-height .48rem
            .score-desc
              font-size .28rem
              color #ff8300
              line-height .48rem
              margin-left .2rem
          .comment
            display flex
            .comment-comment
              font-size .24rem
              color #9e9e9e
              line-height .32rem
              margin-right .2rem
            .comment-raider
              font-size .24rem
              color #9e9e9e
              line-height .32rem
              margin-right .2rem
        .score-icon
          display flex
          float right
          flex-direction column
          justify-content center
          margin-right .1rem
      .intro-content
        position relative
        width 3.55rem
        display flex
        .intro-realcontent
          flex 1
          .intro-desc
            font-size .28rem
            color #212121
            line-height .48rem
            padding-left .3rem
          .intro-time
            color: #9e9e9e
            font-size: .24rem
            padding-left: .3rem
        .intro-icon
          float right
          display flex
          flex-direction column
          justify-content center
          margin-right .1rem
</style>
