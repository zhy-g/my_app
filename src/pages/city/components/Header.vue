<template>
  <div class="header">
      城市选择
      <router-link to='/'>
        <div class="iconfont header-text">
            &#xe618;
        </div>
     </router-link>
  </div>
</template>

<script>
export default {
    name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles'
.header
  position relative
  overflow hidden
  height .86rem
  background-color: $bgColor
  text-align center
  line-height .86rem
  font-size .3rem
  color #fff
  .header-text
    width .64rem
    line-height .86rem
    text-align center
    position absolute
    top 0
    left 0
    color #fff

</style>