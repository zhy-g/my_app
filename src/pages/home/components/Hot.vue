<template>
    <div>
        <div class="title">
            <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" />
            <span class='title-left'>本周热门榜单</span>
            <span class="title-right">全部榜单</span>
        </div>
        <div class="wrapper">
            <swiper :options='swiperOption'>
                <swiper-slide v-for="item of hotList" :key="item.id">
                    <div class="hot-img">
                        <img class='hot-img-content' :src="item.imgUrl">
                    </div>
                    <p class='desc' >{{ item.desc }} </p>
                    <p class='price'> {{ item.price }}<span>起</span></p>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'HomeHot',
        data () {
            return {
                swiperOption: {
                    slidesPerView: 3.5,
                    conteredSlides: false
                },
                hotList: [
                    {
                        id: '001',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/201402/25/7c223b024b7ba7db02088e3f62c5e07c.jpg_250x250_3c9bc297.jpg",
                        desc: '崀山',
                        price: '￥68'
                    },
                    {
                        id: '002',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/1505/e6/e688db1f82f6289f.water.jpg_250x250_fce242ac.jpg",
                        desc: '崀山风景名胜区',
                        price: '￥68'
                    },
                    {
                        id: '003',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/1906/6b/6bc2da1846468108a3.img.jpg_250x250_7405d6f6.jpg",
                        desc: '邵阳市体育新城冰雪公园',
                        price: '￥45'
                    },
                    {
                        id: '004',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/1911/d0/d0713a64b8a02fe9a3.img.png_250x250_e4e09e7e.png",
                        desc: '青木湾微度假生活馆',
                        price: '￥29'
                    },
                    {
                        id: '005',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/1903/7b/7bed58d0da4e5a36a3.img.png_250x250_48edf7d8.png",
                        desc: '大东山滑翔伞基地',
                        price: '￥100'
                    },
                    {
                        id: '006',
                        imgUrl: "http://img1.qunarzz.com/sight/p82/201211/01/33c02177caba84f593835fbb.jpg_250x250_1dcbfb5a.jpg",
                        desc: '辣椒峰',
                        price: '￥7'
                    },
                    {
                        id: '007',
                        imgUrl: "http://img1.qunarzz.com/sight/p0/201403/11/cb414dbafe88c65ab18197ba5c2f85e1.jpg_250x250_7a8b4d44.jpg",
                        desc: '邵阳石门山',
                        price: '￥100'
                    }
                ]
            }
        }

    }
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
  .title
    position relative
    padding .2rem
    padding-bottom -.1rem
    .title-left
      font-size .32rem
      line-height .44rem
    .title-img
      display inline-block
      overflow hidden
      width .3rem
      height .3rem
      verical-align: top
    .title-right
      float right
      color #616161
      font-size .24rem
      line-height .28rem
      position absolute
      top .36rem
      right .32rem
    .wrapper
      height 0
      padding-bottom 40%
      overflow hidden
      width 100%
      .hot-img 
        overflow hidden
        height 26%
        margin-top -.2rem
        .hot-img-content
          margin .15rem
          width 100%
          height 100%
    .desc
      text-align center
      font-size .24rem
      margin-top .12rem
      line-height .32rem
      color #212121
      ellipsis()
    .price
      text-align center
      color #ff8300
      span 
        color #212121
        font-size .24rem
</style>
