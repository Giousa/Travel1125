<template>

  <div>

    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>

    <div>Home首页</div>

  </div>

</template>

<script>

import HomeHeader from './components/Head'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
}

</script>

<style scoped>

</style>
