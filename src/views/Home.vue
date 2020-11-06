<template>
  <Header/>
  <Swiper/>
</template>

<script>
import Header from '../components/Header.vue'
import Swiper from '../components/Swiper.vue'

export default {
  name: 'Home',
  components: { Swiper, Header }
}
</script>
