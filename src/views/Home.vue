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
</template>

<script lang='ts'>
import Header from '../components/Header.vue';
import ProjectProcess from '../components/Home/ProjectProcess.vue';
import ProjectsCase from '../components/Home/ProjectsCase.vue';
import Swiper from '../components/Swiper.vue';
import HomeCenter from '../components/Home/HomeCenter.vue';

export default {
  name: 'Home',
  components: {ProjectProcess, ProjectsCase, Swiper, Header, HomeCenter},
};
</script>

<style lang='scss' scoped>
.line-wrapper {
  border-bottom: 2px solid #e0e0e0;
}
</style>