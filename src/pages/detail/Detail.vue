<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-info></detail-info>
    <detail-position></detail-position>
    <detail-recommend></detail-recommend>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailInfo from './components/Info'
import DetailPosition from './components/Position'
import DetailRecommend from './components/Recommend'

export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailInfo,
    DetailPosition,
    DetailRecommend,
    DetailList
  },
  data () {
    return {
      list: [
        {
          title: '特惠-限量票',
          children: [
            {
              title: '【限量特惠】上海迪士尼儿童票',
              price: '288'
            }, {
              title: '【限量8折】上海迪士尼成人一日票',
              price: '575'
            }, {
              title: '【限量8折】上海迪士尼儿童/老人一日票',
              price: '399'
            }, {
              title: '【限量特惠】上海迪士尼特价票',
              price: '299'
            }
          ]
        }, {
          title: '特惠-夏末票'
        }, {
          title: '必买-餐券'
        }, {
          title: '特惠-半日票'
        }, {
          title: '标准-门票'
        }, {
          title: '音乐剧-美女与野兽'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped></style>
