<template>
    <div class="wrapper">
     <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide>
    <img class='swiper-img' src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/c8762210baff5ade1a3b2fe0ab914992.png_750x200_9bbb2f51.png' />
    </swiper-slide>
    <swiper-slide>
    <img class='swiper-img' src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/1d8faa9f4d49b77ca1e61e2b478260f7.jpg_750x200_25cf76e2.jpg'/>
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/e7eac5a5e99e6517c61b953c0fece63b.jpg_750x200_4b701cf8.jpg">
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/2b3a9445cc37885eb13e0402baef9f5e.png_750x200_24df2b41.png" alt="">
    </swiper-slide>
    <!-- Optional controls -->
   
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper> </div>
</template>


<script>
export default {
  name: 'HomeSwiper',
  data() {
    return {
      swiperOption:{}
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
