<template>
    <div>
        <div class="title">
            <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png">
            <span class="title-content">猜你喜欢</span>
            <ul>
                <li class="item" v-for='item of list' :key="item.id">
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
    props: {
      list: Array
    }
    // 删掉likeList数组
}
</script>

<style lang="stylus" scoped>
  .title 
    margin-top: .2rem
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