<template>
  <div class='project-case'>
    <div class="top">
      <img src="http://www.seejoys.net.cn/Tpl/SJ_Home/conf/images/projects.png" alt="">
      <!--      <div class="en">Projects Case</div>-->
      <!--      <div class="cn">项目案例</div>-->
    </div>
    <div class="item-list">
      <div class="item" v-for='item in itemList'>
        <img :src="item.img" alt="">
        <div class="title">{{item.title}}</div>
        <div class="describe">{{item.describe}}</div>
      </div>
    </div>
    <div class="more-wrapper">
      <div class='more'/>
    </div>
  </div>
</template>

<script lang='ts'>
export default {
  name: 'ProjectsCase',
  setup() {
    const itemList = [
      {id: 1, img: 'http://www.seejoys.net.cn/pics/case/case_s_1541585552.png', title: '保时捷小程序', describe: '我是保时捷小程序'},
      {id: 2, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '通道商城', describe: '我是保时捷小程序'},
      {id: 3, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '天天洗衣', describe: '我是保时捷小程序'},
      {id: 4, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '洗车吧', describe: '我是保时捷小程序'},
      {id: 5, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '拉茶风味', describe: '我是保时捷小程序'},
      {id: 6, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '美团', describe: '我是保时捷小程序'},
      {id: 7, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '茜茜够', describe: '我是保时捷小程序'},
      {id: 8, img: 'http://www.seejoys.net.cn/pics/case/case_s_1539933722.png', title: '探花', describe: '我是保时捷小程序'},
    ];
    return {itemList};
  },
};
</script>

<style lang='scss' scoped>
.project-case {
  width: 1200px;
  padding: 80px 0;
  margin: 0 auto;
  
  > .top {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: 40px;
  }
  
  > .item-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    
    > .item {
      margin-bottom: 40px;
      
      > .title, .describe {
        text-indent: 1em;
      }
      
      > .title {
        margin: 10px 0;
        font-size: 16px;
        font-weight: bold;
      }
      
      > .describe {
        color: #6e6e6e;
        font-size: 14px;
      }
    }
    
  }
  
  > .more-wrapper {
    display: flex;
    justify-content: center;
    
    > .more {
      width: 100px;
      height: 45px;
      background: url("http://www.seejoys.net.cn/Tpl/SJ_Home/conf/images/lc-icon.png") no-repeat 0 0;
    }
  }
}
</style>