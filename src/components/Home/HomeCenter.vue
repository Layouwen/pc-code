<template>
  <div class="homeCenterWrapper">
    <div class="item" v-for="item in itemList">
      <div class="top" :style="{background: item.bgc}"><img :src="item.img" alt=""></div>
      <div class="title">{{item.title}}</div>
      <div class="english">{{item.en_name}}</div>
      <div class="describe">{{item.describe}}</div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  setup() {
    const itemList = [
      {
        id: 1,
        title: '网站建设',
        bgc: '#58ABB7',
        img: 'http://www.vpcv.com/resource/css/skin/images/ser1.png',
        en_name: 'WEB DESIGNE',
        describe: '企业官方网站、品牌形象网站、 商城、模板型网站、企业定制管理系统',
      },
      {
        id: 2,
        title: '移动开发',
        bgc: '#FF7070',
        img: 'http://www.vpcv.com/resource/css/skin/images/ser2.png',
        en_name: 'MOBILE DEVELOPMENT', describe: '企业官方网站、品牌形象网站、 商城、模板型网站、企业定制管理系统',
      },
      {
        id: 3,
        title: '营销推广',
        bgc: '#FF9D70',
        img: 'http://www.vpcv.com/resource/css/skin/images/ser3.png',
        en_name: 'MARKETING',
        describe: '企业官方网站、品牌形象网站、 商城、模板型网站、企业定制管理系统',
      },
      {
        id: 4,
        title: '配套服务',
        bgc: '#598BAC',
        img: 'http://www.vpcv.com/resource/css/skin/images/ser4.png',
        en_name: 'SERVICE',
        describe: '企业官方网站、品牌形象网站、 商城、模板型网站、企业定制管理系统',
      },
    ];
    return {itemList};
  },
};
</script>

<style lang='scss' scoped>
.homeCenterWrapper {
  display: flex;
  justify-content: space-between;
  width: 1200px;
  margin: 0 auto;
  padding: 80px 0;
  
  > .item {
    display: flex;
    flex-direction: column;
    align-items: center;
    
    &:not(:last-child) {
      margin-right: 60px;
    }
    
    > .top {
      width: 130px;
      height: 130px;
      margin-bottom: 20px;
      border-radius: 50%;
    }
    
    > .title {
      font-size: 22px;
    }
    
    > .english {
      margin: 10px 0;
      font-size: 14px;
      color: #ff8309;
    }
    
    > .describe {
      text-indent: 2em;
    }
  }
}
</style>