<template>
    <div>
       <home-header></home-header>
       <home-swiper></home-swiper>
       <home-icons></home-icons>
       <home-hot></home-hot>
       <home-like></home-like>
       <home-place></home-place>
    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/Hot'
import HomeLike from './components/Like'
import HomePlace from './components/place'

export default {
    name: 'Home',
    components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeHot,
      HomeLike,
      HomePlace
    }
}
</script>
<style scoped>

</style>