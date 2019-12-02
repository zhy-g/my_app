<template>
    <div>
        <div class="title">
            <div class="title-content">
                周末去哪儿
            </div>
            <div class="item" v-for="item of list" :key="item.id">
                <img class="item-img" :src="item.imgUrl" alt="">
                <div class="item-info">
                    <p class="item-title">{{ item.title }}</p>
                    <p class="item-content">
                       {{item.content}}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomePlace',
    props: {
        list: Array
    }
    // 删掉placeList数组
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .title
    .title-content
    //   background #eeeeee
      text-indent 1.8em
      height 2.5em
      line-height 2.5em
    .item
      width: 100%
      .item-img
        width 100%
      .item-info
        height 4.3em
        text-indent .8em
        .item-title
          line-height 2em
        .item-content  
          color #666
          font-size 12px
          height 2.3em
          ellipsis()
</style>>