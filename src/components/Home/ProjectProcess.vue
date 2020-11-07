<template>
  <div class='project-process'>
    <div class="top"><img src="http://www.seejoys.net.cn/Tpl/SJ_Home/conf/images/p.jpg" alt=""></div>
    <ul class="title-list">
      <li class="title">签订合同</li>
      <li class="title">项目启动</li>
      <li class="title">产品原型</li>
      <li class="title">视觉图</li>
      <li class="title">研发</li>
      <li class="title">测试</li>
      <li class="title">验收</li>
      <li class="title">上线</li>
    </ul>
    <div class='img'></div>
  </div>
</template>

<script lang='ts'>
export default {
  name: 'ProjectProcess',
};
</script>

<style lang='scss' scoped>
.project-process {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 1200px;
  padding: 80px 0;
  margin: 0 auto;
  
  > .top {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  > .title-list {
    display: flex;
    margin-top: 50px;
    
    > .title {
      width: 135px;
      text-align: center;
      font-size: 22px;
      color: #232729;
    }
  }
  
  > .img {
    width: 1061px;
    height: 148px;
    background: url("http://www.seejoys.net.cn/Tpl/SJ_Home/conf/images/lc-icon.png") no-repeat 0 -40px;
  }
}
</style>