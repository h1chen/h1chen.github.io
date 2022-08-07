<!--
/****************************************************************************
所属系统: 简历
所属模块: 基本信息
创建时间: 2022年02月09日 22:12
维护人: 张和潮
***************************************************************************/
-->
<template>
  <div class="base">
    <h2>张和潮</h2>

    <p class="base__info">
      <span>男</span>
      <span>广东普宁</span>
      <span>本科</span>
      <span>韶关学院</span>
      <span>电子信息科学与技术</span>
    </p>

    <p class="base__desc">“主要从事 B 端后台管理系统以及 Electron 客户端开发。个人技术栈主要以 Vue 为主，平时喜欢钻研 Vue 源码以及最新的前端技术，热衷于在 github 里学习热门的开源项目。”</p>

    <div class="base__work">
      <div class="base__work-text">
        <strong>求职意愿</strong>：
        <span>前端开发</span>
      </div>

      <div>
        <strong>工作年限</strong>：
        <span>三年</span>
      </div>
    </div>

    <div class="base__connect">
        <strong class="base__connect--justilfy">微信</strong>：
        <span class="base__connect-text">13622450494</span>

        <strong class="base__connect--justilfy">邮箱</strong>：
        <span class="base__connect-text">1029267498@qq.com</span>
       
        <strong>github</strong>：
        <a 
           target="_blank"
           class="base__connect-text" 
           href="https://github.com/Rhodri-hc" 
        >https://github.com/Rhodri-hc</a>
    </div>

    
  </div>
</template>
<script>
export default {
  name: "base",
  components: {},
  mixins: [],
  props:{},
  data() {
    return {};
  },
  computed: {},
  created() {},
  mounted() {},
  methods: {}
};
</script>
<style scoped lang="scss">
.base{
  &__info{
    & > span{
      margin-right: 15px;
    } 
  }

  &__work{
    display: flex;
    margin-top: -5px;
    &-text{
      margin-right: 54px;
    }
  }

  &__connect{
    &-text{
      margin-right: 20px;
      text-decoration:none
    }
    

    &--justilfy{
      display: inline-block;
      min-width: 64px;
      text-align-last: justify;
    }
  }

  &__desc{
    line-height: 26px;
    font-style: italic;
    font-size: 15px;
    margin-top: -10px;
  }

}
</style>
