<!--
/****************************************************************************
所属系统: 简历
所属模块: 简历主页
创建时间: 2022年02月09日 21:44
维护人: 张和潮
***************************************************************************/
-->
<template>
  <Base></Base>

  <Skill></Skill>

  <Project></Project>
  
  <Experience></Experience>
</template>

<script>
// 个人基本信息
import Base from "./components/base";
// 技能清单
import Skill from "./components/skill";
// 项目经验
import Project from "./components/project";
// 工作经历
import Experience from "./components/experience"

export default {
  name: "resume",
  components: {Base, Skill, Project, Experience},
  mixins: [],
  data() {
    return {};
  },
  computed: {},
  created() {},
  mounted() {},
  methods: {}
};
</script>
<style scoped lang="scss"></style>
