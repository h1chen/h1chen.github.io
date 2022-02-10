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
        "熟练使用Vue.js框架开发项目，熟悉Vue.js全家桶；",
        "熟练使用Element-UI等前端框架，具有开发前端组件库经验；",
        "懂得使用Electron构建桌面应用程序；",
        "懂得使用Tailwind CSS框架，了解Scss，Stylus等CSS预处理器；"
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
}


</style>
