<template>
    <div>
      <!-- 通过绑定city属性来传值 -->
       <home-header :city="city"></home-header>
       <!-- 绑定list来床底swiperList数据 -->
       <home-swiper :list='swiperList'></home-swiper>
       <home-icons :list='iconList'></home-icons>
       <home-hot :list='hotList'></home-hot>
       <home-like :list='likeList'></home-like>
       <home-place :list='placeList'></home-place>

    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/Hot'
import HomeLike from './components/Like'
import HomePlace from './components/place'
//引入axios
import axios from 'axios'


export default {
    name: 'Home',
    components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeHot,
      HomeLike,
      HomePlace
    },
    data () {
      // 在Home.vue中的data函数中初始化数据
      return {
        city: '',
        swiperList: [],
        iconList: [],
        hotList: [],
        likeList: [],
        placeList: [],
      }
    },
    // 在methods中定义函数getHomeInfo()
    methods: {
      getHomeInfo () {
          axios.get('/api/index.json').then(this.getHomeInfoSucc)
          // static目录下的文件可以在地址栏上直接访问，src目录下文件不能直接访问，
          // 但是从上线和安全角度考虑我们需要使用代理转发机制将真实的访问目录隐藏替换成api
          // 我们可以在config目录下的index.js文件里proxyTable里实现这个功能
      },
      // getHomeInfoSucc会将获取成功的数据打印
      getHomeInfoSucc(res) {
        // 统一获取页面模拟的数据
        res = res.data
        if(res.ret && res.data) {
          // 判定res.ret返回是够真并且数据是否存在
          const data = res.data
          this.city = data.city
          this.swiperList = data.swiperList
          this.hotList = data.hotList
          this.iconList = data.iconList
          this.likeList = data.likeList
          this.placeList = data.placeList
        }
      }
    },
    // 生命周期函数mounted
    mounted () {
      // 在生命周期中执行getHomeInfo函数
      this.getHomeInfo()
    }
}
</script>
<style scoped>

</style>