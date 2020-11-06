<template>
  <header>
    <div class="logo"></div>
    <div class="search">
      <a-input-search
        v-model:value="inputValue"
        placeholder="请输入搜索内容"
        enter-button
        @search="onSearch"
      />
    </div>
    <nav>
      <a v-for="(nav, index) in navList"
         :href="nav.url"
         :class="{'active': activeIndex === index}"
         @click="changeIndex(nav.url)"
      >{{nav
        .title}}</a>
    </nav>
  </header>
</template>

<script lang='ts'>
import {ref} from 'vue';

export default {
  setup() {
    const activeIndex = ref(0);
    const inputValue = ref('');
    const navList = [
      {url: 'javascript:', title: '主页'},
      {url: 'javascript:', title: '关于我们'},
      {url: 'javascript:', title: '成功案例'},
      {url: 'javascript:', title: '网站资讯'},
      {url: 'javascript:', title: '小程序'},
      {url: 'javascript:', title: '联系我们'},
    ];
    const changeIndex = (url) => {
      console.log(url);
    };
    const onSearch = inputData => {
      console.log('你搜索的内容是', inputData);
    };
    return {activeIndex, navList, changeIndex, inputValue, onSearch};
  },
};
</script>

<style lang='scss' scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 1200px;
  margin: 0 auto;
  
  .logo {
    width: 230px;
    height: 70px;
    background: red;
  }
  
  .search {
    width: 300px;
  }
  
  nav {
    > a {
      margin: 0 20px;
      
      &.active {
        color: red;
      }
    }
  }
}
</style>
