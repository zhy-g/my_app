<template>
    <div class="icons">
        <div class="icon">
            <div class="icon-img">
                <img src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" class="icon-img-content">
            </div>
            <div class="icons-desc">景点门票</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png" class="icon-img-content">
            </div>
            <div class="icons-desc">自然风光</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img src="http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png" class="icon-img-content">
            </div>
            <div class="icons-desc">当地好玩</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img src="http://img1.qunarzz.com/piao/fusion/1803/ee/5114069893722102.png" class="icon-img-content">
            </div>
            <div class="icons-desc">游山玩水</div>
        </div>
        <div class="icon">
            <div class="icon-img">
                <img src="http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png" class="icon-img-content">
            </div>
            <div class="icons-desc">全部玩乐</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  .icons
    overflow hidden
    height: 0
    padding-top 2%
    padding-bottom  50%
    // background #eeeeee
    // icons层样式
    .icon
      position: relative
      overflow hidden
      float left
      width 22%
      height 0
      padding-bottom: 20%
      padding-left 3%
    // 单个icon层样式
    .icon-img
      position absolute
      top 0
      left 0
      right 0
      bottom .44rem
      box-sizing border-box
      .icon-img-content
        display block
        margin 0 auto 
        height: 100%
    .icons-desc
      position: absolute
      left 0
      right 0
      bottom 0
      heigth .44rem
      line-height .44rem
      text-align center
</style>