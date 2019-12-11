<template>
    <!-- 添加ref -->

    <div class="list" ref="wrapper">
      <div>
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>
        </div>
        <div class="area">
            <div class="title border-topbottom">热门城市</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>
        </div>
        <div class="area">
            <div class="title border-topbottom">B</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>
        </div>
      </div>
    </div>
</template>

<script>
// 添加btter-scroll
import Bscroll from 'better-scroll'

export default {
    name: 'CityList',
    // 添加声明周期函数并调用
    mounted () {
      this.scroll = new Bscroll(this.$refs.wrapper)
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles'
  .border-topbottom
    &:before
      border-color #cccccc
    &:after
      border-color #cccccc
  .border-topbottom 
    &:after
      border-color #cccccc
    // 添加.list类
  .list
    position: absolute 
    overflow hidden
    top: 1.58rem
    left: 0
    right 0
    bottom 0
    .title
      line-height .44rem
      background #eee
      padding-left .2rem
      color #666
      font-size .26rem
    .button-list
     overflow hidden
     padding .1rem .6rem .1rem .1rem
    .button-wrapper
      float left
      width 33.33%
      .button
        text-align center
        margin 0.1rem
        padding .1rem 0
        border .02rem solid #cccccc
        border-radius .08rem
  .item-list
    .item 
      line-height .54rem
</style>