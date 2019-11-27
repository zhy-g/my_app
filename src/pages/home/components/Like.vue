<template>
    <div>
        <div class="title">
            <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png">
            <span class="title-content">猜你喜欢</span>
            <ul>
                <li class="item" v-for='item of likeList' :key="item.id">
                    <img :src="item.imgUrl" class="item-img" alt="">
                    <div class="item-info">
                        <p class="item-title">{{ item.title }}</p>
                        <p>
                            <span class="iconfont" v-html="item.start">{{ item.star }}</span>
                            <!-- 因为data里返回的数据类型并不会直接识别为代码，所有我们需要用到v-html识别星星的代码 -->
                            <span class="item-comment">{{ item.comment }}</span>
                        </p>
                        <p class="item-price">
                            <em>￥</em>
                            {{ item.price }}<span>起</span>
                        </p>
                        <p class="item-desc"> {{ item.desc }} </p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeLike',
    data () {
        return {
            likeList: [
             {
                id: '001',
                imgUrl: "http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg",
                title: '故宫',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '562196条评论',
                price: '40',
                desc: '世界五大宫之首，穿越与您近在咫尺'
             },
             {
                id: '002',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg',
                title: '八达岭长城',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '95921条评论',
                price: '35',
                desc: '不到长城非好汉'
             },
             {
                id: '003',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1911/29/29d9b9078000774fa3.img.jpg_200x200_3621a35a.jpg',
                title: '北京欢乐谷',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '82621条评论',
                price: '145',
                desc: '亚洲唯一飞行式过山车等你来挑战'
             },
             {
                id: '004',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
                title: '北京野生动物园',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '30772条评论',
                price: '122',
                desc: '敢与森林之王近距离接触吗？'
             },
             {
                id: '005',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/5d/5dcaf453dfd6f5dba3.img.jpg_200x200_51d03f19.jpg',
                title: '古北水镇',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '14102条评论',
                price: '140',
                desc: ''
             },
             {
                id: '006',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/68/68aa05adb5315f9990.water.jpg_200x200_ce3d2658.jpg',
                title: '北京海洋馆',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '9028条评论',
                price: '170',
                desc: ''
             },
             {
                id: '007',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_200x200_c62292e9.jpg',
                title: '北京动物园',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '11283条评论',
                price: '170',
                desc: ''
             },
             {
                id: '008',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/85/85c883189bf7293390.water.jpg_200x200_3165123d.jpg',
                title: '什刹海',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '4647条评论',
                price: '5',
                desc: ''
             },
             {
                id: '009',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1910/6a/6a22d154133b1422a3.water.jpg_200x200_eebf77fd.jpg',
                title: '北京杜莎夫人蜡像馆',
                start: '&#xe718;&#xe718;&#xe718;&#xe718;&#xe718;',
                comment: '9926条评论',
                price: '146',
                desc: '听说能遇到杰伦哦'
             }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
  .title 
    margin-top: .2rem
    background #eee
    padding .2rem
    .title-img 
      width .3rem
      height .3rem
      margin-top -.09rem
    .title-content 
      margin-left .08rem
      height .44rem
      color red
      font-size .32rem
      line-height .44rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    padding-bottom 1rem
    border-bottom 1px solid #ccc
    .item-img
      width 2rem
      height 2rem
      padding .2rem
    .item-info
      flex 1
      padding .1rem
      margin-top .3rem
      min-width 0
      .item-title
        height .44rem
        color #212121
        font-size .32rem
        line-height .44rem
        margin-bottom .1rem
      .iconfont 
        color #ffb436
        font-size .25rem
      .item-comment
        color #212121
        margin-left .2rem
      .item-price
        font-size .4rem
        color #ffb436
        margin-top .2rem
        em
          font-size .25rem
        span
          color #616161
          font-sie .25rem
      .item-desc
        margin-top .6rem
        color #f55
        font-size .24rem
</style>