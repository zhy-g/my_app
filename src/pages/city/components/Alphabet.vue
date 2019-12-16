<template>
    <ul class="list">
        <!-- 通过v-for循环遍历传递出来的cities里的数据 -->
          <!-- v-for="(item,key) of cities" -->
            <!-- :key="key" -->
        <li class="item" 
        v-for="item of letters"
        :key="item"
        :ref="item"
        @click="handleLetterClick"
        @touchstart='handleTouchStart'
        @touchmove="handleTouchMove"
        @touchend="handleTouchEnd"> 
        <!-- {{ key }} </li> -->
        {{ item }}</li>
        <!--  通过click事件绑定对应的点击事件和触屏事件方法 -->
    </ul>
</template>

<script>
export default {
    name: 'CityAlphabet',
    // props指定传递的数据的类型
    props: {
        cities: Object
    },
    computed: {
        letters () {
            const letters = []
            for (let i in this.cities) {
                letters.push(i)
            }
            return letters
        }
    },
    // 初始化data数据，设定触屏状态为false
    data () {
        return {
            touchStatus: false
        }
    },
    // 处理点击事件和触屏事件的方法
    methods: {
        // 处理字母单击函数
        handleLetterClick (e) {
            // 通过$emit触发change事件并传入单击事件获取的参数
            this.$emit('change', e.target.innerText)
            console.log(e)
            // console.log(e.target.innerText)
            // 输出通过点击获取到的参数e
        },
        // 设定触屏开始，将状态为true
        handleTouchStart () {
            this.touchStatus = true
           
        },
        // 处理触屏移动事件，接受参数e
        //  startY为获取字母A的顶点位置参数
        // touchY为
        handleTouchMove (e) { 
            const startY = this.$refs['A'][0].offsetTop
            // console.log(startY)
            const touchY = e.touches[0].clientY - 79
            // console.log(touchY)
            const index = Math.floor(( touchY - startY) / 20)
            if (index >=0 && index < this.letters.length) {
                this.$emit('change', this.letters[index])
            }console.log(e)
            console.log(index)
        },
        // 触屏状态结束，将状态设为false
        handleTouchEnd () {
            this.touchStatus = false
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles'
  .list
    display flex
    flex-direction column
    justify-content center
    position absolute 
    top 1.58rem
    right 0
    bottom 0
    width .4rem
    .item
      text-align center
      line-height .4rem
      color $bgColor
</style>