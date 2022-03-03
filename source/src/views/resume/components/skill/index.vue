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
        "熟练 Vue.js 前端开发框架，熟练使用 Vue.js 全家桶；",
        "熟练 Element-UI 等前端框架，具有开发前端组件库经验；",
        "熟悉 Electron 构建桌面应用程序；",
        "熟悉 Tailwind CSS 框架，以及 Scss，Stylus 等 CSS 预处理器；",
        "熟悉前端性能优化方法，熟悉 Http 协议，熟悉各种 Web 标准规范；",
        "熟悉移动端与 PC 端的适配工作",
        "熟悉 ESLint 等代码检查工具的配置及使用，有良好的代码习惯；",
        "了解小程序开发框架，具有小程序开发经验；",
        "了解 webpack 构建工具；",
        "了解 Node.js 开发语言；"
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
    
  }
}


</style>
