<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for='(page, index) of pages'  :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div class="icon-img">
                        <img :src="item.imgUrl" class="icon-img-content">
                    </div>
                    <p class="icons-desc">{{ item.desc }}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    props: {
        list: Array
    },

    data () {
        return {
            swiperOption: {
                // autoplay自动播放除了有ture和false值以外， 还可以直接指定轮播的时间间隔 例如： autoplay: 5000
                autoplay: false
            }
            // 删掉iconList数组
        }
    },            
    computed:{
        pages (){
            const pages = [];
            // 将iconList修改成list
            this.list.forEach((item, index) => {
                const page = Math.floor(index / 8)
                if (!pages[page])
                {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>list

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    overflow hidden
    height: 0
    padding-top 3%
    padding-bottom  43%
    icons层样式
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
      ellipsis()
</style>