<template>
    <div>
       <home-header></home-header>
    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'

export default {
    name: 'Home',
    components: {
      HomeHeader,
      HomeSwiper
    }
}
</script>
<style scoped>

</style>