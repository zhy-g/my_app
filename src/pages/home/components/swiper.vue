<template>
    <div class="wrapper">
      <!-- 添加v-if='list.length'解决初始化空数组导致乱序问题 -->
      <swiper :options="swiperOption" v-if='list.length'>
          <!-- slides -->
          <!-- 将原来循环的swiperList 改成新的list数组 -->
          <swiper-slide v-for='item of list' :key='item.id'>
            <img :src="item.imgUrl" alt="" class="swiper-img">
          </swiper-slide>
          <!-- Optional controls -->
          <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
     </div>
</template>


<script>
export default {
  name: 'HomeSwiper',
  // 指定props里接受list是数组
  props: {
    list: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  }
 
}
</script>

<style lang='stylus'> 
  .wrapper
    overflow hidden
    // padding-bottom 26.66%
    width: 100%
    .swiper-img
     width: 100%
</style>
