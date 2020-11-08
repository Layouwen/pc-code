<template>
  <Header/>
  <Swiper/>
  <div class="line-wrapper">
    <HomeCenter/>
  </div>
  <div class="line-wrapper">
    <ProjectsCase/>
  </div>
  <div class="line-wrapper" style='background: #f1f5f7;'>
    <ProjectProcess/>
  </div>
  <div style='background: #f1f5f7;'>
    <CallMe/>
  </div>
  <Footer/>
</template>

<script lang='ts'>
import Header from '../components/Header.vue';
import Swiper from '../components/Swiper.vue';
import Footer from '../components/Footer.vue';
import HomeCenter from '../components/Home/HomeCenter.vue';
import ProjectsCase from '../components/Home/ProjectsCase.vue';
import ProjectProcess from '../components/Home/ProjectProcess.vue';
import CallMe from '../components/Home/CallMe.vue';

export default {
  name: 'Home',
  components: {CallMe, Footer, ProjectProcess, ProjectsCase, Swiper, Header, HomeCenter},
};
</script>

<style lang='scss' scoped>
.line-wrapper {
  border-bottom: 2px solid #e0e0e0;
}
</style>