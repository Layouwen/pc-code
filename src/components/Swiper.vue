<template>
  <a-carousel effect="fade" autoplay>
    <div class='imgWrapper' v-for="img in imgList"><img :src='img.url'></div>
  </a-carousel>
</template>

<script>

export default {
  name: 'Swiper',
  setup () {
    const imgList = [
      { id: 1, url: 'http://www.seejoys.net.cn/pics/banner/banner_s_1461307907.png' },
      { id: 2, url: 'http://www.seejoys.net.cn/pics/banner/banner_s_1450842050.png' }
    ]
    return { imgList }
  }
}
</script>

<style lang="scss" scoped>
.ant-carousel ::v-deep(.slick-slide) {
  
  .imgWrapper {
    height: 525px;
    
    img {
      height: 525px;
    }
  }
}
</style>