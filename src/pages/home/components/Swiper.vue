<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//img1.qunarzz.com/vc/2a/96/76/d149c7a3a5b113f876f9a66e09.png'
      }, {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/vc/1d/d5/dc/bfb1990e14a1fdb082cf817657.jpg'
      }, {
        id: '0003',
        imgUrl: '//img1.qunarzz.com/vc/a9/f4/f1/bb33ddb697f07c375e7af81256.jpg'
      }, {
        id: '0004',
        imgUrl: '//img1.qunarzz.com/vc/bf/9d/a3/67b7b37511fa26a78298bf1da1.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff !important
  .wrapper
    overflow: hidden
    width:100%
    height: 0
    padding-bottom: 30.5%
    background: #eee
    .swiper-img
      width: 100%
</style>
