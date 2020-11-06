<template>
  <Header/>
  <Swiper/>
  <HomeCenter/>
</template>

<script>
import Header from '../components/Header.vue'
import Swiper from '../components/Swiper.vue'
import HomeCenter from '../components/Home/HomeCenter.vue'

export default {
  name: 'Home',
  components: { Swiper, Header, HomeCenter }
}
</script>
