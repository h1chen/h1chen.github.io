<!--
/****************************************************************************
所属系统: 简历
所属模块: 项目经验
创建时间: 2022年02月09日 22:14
维护人: 张和潮
***************************************************************************/
-->
<template>
  <div class="project">
    <h3 class="project__title">部分项目经验</h3>

<!-- 项目经验内容 -->
    <div  v-for="(item, index) of projectList" class="project__content" :key="index">
      <div class="project__content-title">
        <p class="project__content-name">{{ item.title }}</p>
        <p>{{ item.timeRange }}</p>
      </div>

      <div class="project__content-duty">
        <span class="project__content-label">项目描述：</span>
        <span>{{ item.desc }}</span>
      </div>

      <div class="project__content-duty">
        <span class="project__content-label">职责：</span>
        <div>
          <div v-for="(ele, idx) of item.duty" :key="idx">
            {{ ele }}
          </div> 
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "project",
  components: {},
  mixins: [],
  data() {
    return {
      // 部分项目经验
      projectList:[{
        title: "KPC即时通讯软件",
        timeRange: "（2021.03 - 至今）",
        desc: "项目采用 Electron、Vue框架、node 以及 SQLite 的架构，运用腾讯IM即时通讯服务，自定义消息格式以及公司业务提醒等协议，实现教育培训行业的即时通讯软件。项目包括即时通讯常见的单聊群聊、消息已读未读、群通知以及个人或群信息等功能，还包括公司自己的业务功能。",
        duty: [
          "1. 主导负责项目的整体进度"
        ]
      },{
        title: "运营中心管理系统",
        timeRange: "（2020.09 - 2021.09）",
        desc: "关于运营中心的项目描述",
        duty:[
          "1. 根据自研组件库和技术栈构建项目基础框架"
        ]
      }]
    };
  },
  computed: {},
  created() {},
  mounted() {},
  methods: {}
};
</script>
<style scoped lang="scss">
.project{
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
    padding: 0 20px;
    line-height: 26px;
    margin-top: -5px;
    margin-bottom: 20px;
    &-title{
      display: flex;
      align-items: center;
      margin-bottom: 4px;
      & > p {
        margin: 0;
      }
    }
    &-name{
      font-size: large;
      font-weight: 600;
    }

    &-label{
      font-weight: 550;
      white-space: nowrap;
    }
     &-duty {
      display: flex;
    }
  }
}
</style>
