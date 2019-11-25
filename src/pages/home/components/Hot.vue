<template>
    <div>
        <div class="title">
            <img class="title-img" src="" />
            <span class='title-left'>本周热门榜单</span>
            <span class="title-right">全部榜单</span>
        </div>
        <div class="wrapper">
            <swiper :options='swiperOption'>
                <swiper-slide v-for="item of hotList" :key="item.id">
                    <div class="hot-img">
                        <img class='hot-img-content' :src="item.imgUrl">
                    </div>
                    <p class='desc' {{ item.desc }}> </p>
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
                        imgUrl: "",
                        desc: '崀山',
                        price: '￥68'
                    },
                    {
                        id: '002',
                        imgUrl: "",
                        desc: '崀山风景名胜区',
                        price: '￥68'
                    },
                    {
                        id: '003',
                        imgUrl: "",
                        desc: '邵阳市体育新城冰雪公园',
                        price: '￥45'
                    },
                    {
                        id: '004',
                        imgUrl: "",
                        desc: '青木湾微度假生活馆',
                        price: '￥29'
                    },
                    {
                        id: '005',
                        imgUrl: "",
                        desc: '大东山滑翔伞基地',
                        price: '￥100'
                    },
                    {
                        id: '006',
                        imgUrl: "",
                        desc: '辣椒峰',
                        price: '￥7'
                    },
                    {
                        id: '007',
                        imgUrl: "",
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
        height 24%
        margin-top -.2rem
        .hot-img-content
          margin .15rem
          width 100%
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
