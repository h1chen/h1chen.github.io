<!--
/****************************************************************************
所属系统: 简历
所属模块: 技能清单
创建时间: 2022年02月09日 22:13
维护人: 张和潮
***************************************************************************/
-->
<template>
  <div class="skill">
    <h3 class="skill__title">技能清单</h3>
      <ul 
        v-for="(item, index) of skillList" 
        class="skill__content"
        :key="index"
      >
        <li>{{ item }}</li>
      </ul>
  </div>
</template>
<script>
export default {
  name: "skill",
  components: {},
  mixins: [],
  data() {
    return {
      skillList:[
        "熟练使用 Vue.js 前端开发框架，了解 Vue2、Vue3 核心原理，了解 Nuxt.js 搭建服务端渲染",
        "熟练使用 Vue 主流 UI 框架（Element-UI），并有深入学习经验，具有公司自研组件库开发经验",
        "熟悉 Electron 构建桌面应用程序，熟悉小程序开发框架 ，具有小程序 mpvue 框架开发经验",
        "熟悉前端性能优化方法，熟悉 http、TCP 协议，熟悉各种 Web 标准规范，了解设计模式并运用在开发中",
        "熟悉前端工程化，熟悉使用 webpack 构建工具并了解原理，开发 plugin 解决实际问题",
        "熟悉 ESLint 等代码检查工具的配置及使用，有良好的代码习惯",
        "了解使用 Node.js，对服务端框架 egg.js 编写 BFF 层有开发经验",
      ]
    };
  },
  computed: {},
  created() {},
  mounted() {},
  methods: {}
};
</script>
<style scoped lang="scss">
.skill{
  padding-bottom: 15px;
  border-bottom: 1px solid #000;
  &__title{
    display: flex;
    align-items: center;
    
    &:before{
      content: "";
      display: inline-block;
      width: 15px;
      height: 25px;
      background: #000;
      transform: skewX(-20deg);
      margin-right: 4px;
    }
  }

  &__content{
    margin: 10px 0;
  }
}


</style>
