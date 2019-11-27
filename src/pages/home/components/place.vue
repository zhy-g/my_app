<template>
    <div>
        <div class="title">
            <div class="title-content">
                周末去哪儿
            </div>
            <div class="item" v-for="item of placeList" :key="item.id">
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
    data () {
        return {
            placeList: [
                {
                    id: '001',
                    imgUrl: "http://img1.qunarzz.com/sight/source/1711/2b/d4ebbd8337f1ac.jpg_r_640x214_2d4332c1.jpg",
                    title: "湖南泡汤圣地",
                    content: '山谷自然风幽深，泉水潺潺，宜人的光，怡人的田园景色...'
                },
                {
                    id: '002',
                    imgUrl: 'http://img1.qunarzz.com/sight/source/1509/3a/e163a8e32517d9.jpg_r_640x214_4fd882d3.jpg',
                    title: "边城秋色",
                    content: '不得不看的边城秋日之美'
                },
                {
                    id: '003',
                    imgUrl: 'http://img1.qunarzz.com/sight/source/1811/88/8d3b492ebf0b16.jpg_r_640x214_7b3a281d.jpg',
                    title: "邂逅凤凰城",
                    content: '凤凰古城一个古老而神秘的地方，风景秀丽，历史悠久...'
                },
                {
                    id: '004',
                    imgUrl: 'http://img1.qunarzz.com/sight/source/1811/b4/71c01c98139cf.jpg_r_640x214_30bac495.jpg',
                    title: "亲身体验人间仙境",
                    content: '天骄天地，绝壁高崖之间的高台，台下深不见底的山涧...'
                },
                {
                    id: '005',
                    imgUrl: 'http://img1.qunarzz.com/sight/source/1812/1e/131ba1bc67be3e.jpg_r_640x214_edd2705d.jpg',
                    title: "株洲必打卡",
                    content: '亲身体验株洲当地人最爱的去处'
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .title
    .title-content
      background #eeeeee
      text-indent 1.8em
      height 2em
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