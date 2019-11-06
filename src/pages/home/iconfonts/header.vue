<template>
    <div class="header">
        <div class="header-left">
            <span class="">返回</span>
        </div>
        <div class="header-input">内容</div>
        <div class="header-right">城市</div>
    </div>
</template>

<script>
export default {
    name: 'HomeHeader',
    components: {
      HomeHeader
    }
}
</script>

<style lang="stylus" scoped>
  .header
    height: .88rem
    background: #00bcd4
    .header-left
      float left
    .header-input
      background #ffffff
    .header-right
      float right
</style>