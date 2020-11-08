<template>
  <div class="call-me">
    <div class="left">
      <h3 class="wechat">微信公众号</h3>
      <div class="code-wrapper"></div>
      <span>扫一扫</span>
    </div>
    <div class='form-wrapper'>
      <h3>您有需要来告诉我们</h3>
      <div class="wrapper">
        <a-input v-model:value="name" placeholder="姓名"/>
        <a-input v-model:value="phone" placeholder="电话"/>
      </div>
      <a-textarea v-model:value="answer" placeholder="请在这里输入您的需求、您的资料我们会保密处理并尽快回复。" showCount :maxlength="100"/>
      <a-button type="primary" @click="submit">发送给我们</a-button>
    </div>
    <div class="business">
      <h3>我们的业务</h3>
      <ul>
        <li>APP定制</li>
        <li>系统开发</li>
        <li>网站建设</li>
        <li>微信开发</li>
        <li>企业服务</li>
      </ul>
    </div>
    <div class="right">
      <h3>联系我们</h3>
    </div>
  </div>
</template>

<script lang='ts'>
import {ref} from 'vue';

export default {
  name: 'CallMe',
  setup() {
    const name = ref('');
    const phone = ref('');
    const answer = ref('');
    const submit = () => {
      console.log(name.value, phone.value, answer.value);
    };
    return {name, phone, answer, submit};
  },
};
</script>

<style lang="scss" scoped>
.call-me {
  display: flex;
  justify-content: space-between;
  width: 1200px;
  margin: 0 auto;
  padding: 80px 0;
  
  > .left > h3,
  > .business > h3,
  > .form-wrapper > h3,
  > .right > h3 {
    font-size: 18px;
    color: #333;
    font-weight: lighter;
  }
  
  > .left {
    > .wechat {
    }
    
    > .code-wrapper {
      width: 110px;
      height: 110px;
      margin-bottom: 20px;
      background: #fff;
    }
  }
  
  > .form-wrapper {
    > .wrapper {
      display: flex;
      margin-bottom: 20px;
      
      > .ant-input:first-child {
        margin-right: 20px;
      }
    }
  }
  
  > .business {
  }
  
  > .right {
  
  }
}
</style>