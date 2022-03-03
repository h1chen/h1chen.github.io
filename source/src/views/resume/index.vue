<!--
/****************************************************************************
所属系统: 简历
所属模块: 简历主页
创建时间: 2022年02月09日 21:44
维护人: 张和潮
***************************************************************************/
-->
<template>
  <div>
    <div 
      class="content" 
      ref="content" 
      :class="{ 'content--pdf' : isPdf }"
    >
      <Base></Base>

      <Skill></Skill>

      <Project></Project>
      
      <Experience></Experience>
    </div>

    <div class="content__buttons">
      <div class="content__buttons-btn" @click="clickToPDF">PDF</div>
      <div class="content__buttons-btn" @click="clickToPrint">打印</div>
    </div>

    <HtmlToPdf ref="toPdf"></HtmlToPdf>
  </div>

</template>

<script>
// 个人基本信息
import Base from "./components/base";
// 技能清单
import Skill from "./components/skill";
// 项目经验
import Project from "./components/project";
// 工作经历
import Experience from "./components/experience";

// pdf
import HtmlToPdf from "../../components/htmlToPdf"
// 打印
import { print } from "../../utils/print.js"

export default {
  name: "resume",
  components: {Base, Skill, Project, Experience, HtmlToPdf},
  mixins: [],
  data() {
    return {
      // 正在打印pdf
      isPdf: true
    };
  },
  computed: {},
  created() {},
  mounted() {},
  methods: {
    /**
    * @desc 点击pdf
    * @author 张和潮
    * @date 2022年02月23日 16:17
    */
    async clickToPDF(){
      this.isPdf = true;
      await this.$refs.toPdf.downloadPDF(
          this.$refs.content,
          "张和潮简历"
      );
      this.isPdf = false;
    },
    /**
     * @desc 点击打印
     * @author 张和潮
     * @date 2022年02月23日 20:29
     */
    clickToPrint(){
      print(this.$refs.content)
    }
  }
};
</script>

<style scoped lang="scss">
.content{
  position: relative;
  width: 800px;
  margin: 0 auto;
  &__buttons{
    position: fixed;
    right: 80px;
    bottom: 50px;
    display: flex;
    &-btn{
      cursor: pointer;
      padding: 5px 10px;
      border: 1px solid saddlebrown;
      border-radius: 4px;
      margin-right: 15px;
    }
  }

  &--pdf{
    padding: 2px 20px 15px;
  }
  
}
</style>
