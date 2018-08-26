<template>
  <div class="position">
    <div class="address-icon">
      <span class="iconfont">&#xe67a;</span>
    </div>
    <div class="text">
      <span>上海市浦东新区川沙新镇上海迪士尼度假区内</span>
    </div>
    <div class="arrow-icon">
      <span class="iconfont">&#xe600;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DatailPosition'
}
</script>

<style lang="stylus" scoped>
  .position
    display flex
    position relative
    padding .1rem 0 .2rem 0
    line-height .36rem
    .address-icon
      float left
      padding-left .4rem
      line-height .36rem
      color #9e9e9e
    .text
      flex 1
      text-align center
    .arrow-icon
      float right
      margin-right .3rem
</style>
