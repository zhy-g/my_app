<template>
    <div class="header">
        <div class="header-left">
            <span class="iconfont back-icon">&#xe618;</span>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe633;</span>输入城市/景点/游玩主题
        </div>
        <div class="header-right">城市
          <span class="iconfont arrow-icon">&#xe60c;</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
 .header
    display: flex
    line-height: .88rem
    background: $bgColor
    color: #fff
    .header-left
      text-align center
      width: 0.6rem
      float: left
      .back-icon
        float right
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem

</style>