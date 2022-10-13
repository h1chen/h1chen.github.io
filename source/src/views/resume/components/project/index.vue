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
        <span class="project__content-label">项目描述</span>：
        <span>{{ item.desc }}</span>
      </div>
      
      <div class="project__content-duty">
        <span class="project__content-label">涉及技术</span>：
        <span class="project__content-technology">{{ item.technology }}</span>
      </div>

      <div class="project__content-duty">
        <span class="project__content-label">职责</span>：
        <div>
          <div v-for="(ele, idx) of item.duty" :key="idx">
            {{ ele }}
          </div> 
        </div>
      </div>
     
      <div class="project__content-duty">
        <span class="project__content-label">项目成就</span>：
        <div>
          <div v-for="(ele, idx) of item.achievement" :key="idx">
            {{ ele }}
          </div> 
        </div>
      </div>

      <div v-if="item.link" class="project__content-duty">
        <span class="project__content-label">项目链接</span>：
        <a :href="item.link" target="_blank">{{ item.link }}</a>
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
      projectList:[
        {
          title: "运营中心管理系统",
          timeRange: "（2020.09 - 2021.01）",
          desc: "项目面向运营管理部门使用，其中主要分为督导校区巡查和校区权益金管理两大模块，用于教育总部巡查管理校区办学情况以及校区权益金管理，更直观便捷掌握各办学校区情况。",
          technology: "Vue.js、自研组件库",
          duty:[
            "1. 负责督导巡查评分模块、月营业额报表以及权限控制等模块开发",
            "2. 细化需求划分和共用组件抽离，使用 VuePress 生成 UI 组件管理文档",
            "3. 负责通过优化组件配置完成开发以及改进和优化开发工具",
            "4. 封装 http 请求异常，覆盖 FCP/LCP/TTL 指标和白屏，打包后配合 analyzer 页面的分析，对首屏渲染、缓存策略、代码打包进行优化",
            "5. 使用 echarts 对校区运营数据进行可视化处理",
            "6. 统一代码规范和流程，负责定期参与项目代码 review ，保证项目代码质量"
          ],
          achievement: [
           "1. 得到校区督导的正向反馈，提高了督导的工作效率",
           "2. 总部对各校区权益金管理更加合理方便，大大提高了运营部门的工作效率，从而为公司带来了效益",
           "3. 项目首屏渲染时间从 3s 下降到 1s 内，性能指标平均提升 20%，项目体积减少 15%"
          ]
        },
        {
          title: "人事管理系统",
          timeRange: "（2021.01 - 2021.06）",
          desc: "项目面向企业人事管理部门使用，其中主要分为员工考勤打卡、员工档案管理、员工薪资管理以及人事异动模块，用于方便人事部门规范人事以及档案管理。更加直观掌握企业员工信息。",
          technology: "Vue2/3、Tailwind、自研组件库",
          duty:[
            "1. 推动部分业务线进行 Vue3 + Tailwind CSS 重构, 参与代码 review",
            "2. 负责员工考勤模块、员工档案管理等模块开发",
            "3. 负责员工档案编辑展示组件开发，员工打卡 H5 等页面开发",
            "4. 通过 WebWorker 处理批量运算，解决界面渲染卡顿、掉帧假死状态",
            "5. 优化 Webpack 配置，抽离第三方插件，将有效降低打包时间，资源降低 30%"
          ],
          achievement: [
           "1. 方便了员工的考勤与请假流程，得到了员工和人事部门的正向反馈，提高了人事部门的办事效率"
          ]
        },
        {
          title: "杰人软件组件库（jerri-ui）",
          timeRange: "（2020.10 - 至今）",
          desc: "用于最大限度的减轻前端重复开发工作量，为了统一样式标准并且使前端组的每一位同事都能在这里快速的找到自己想到的东西而共同开发的“前端弹药库”",
          technology: "Vue.js",
          duty:[
            "1. 负责下拉框，输入框以及表单等组件的开发",
            "2. 负责创建常见页面操场模板，供开发直接复制改写",
            "3. 负责组件库文档的编写以及更新"
          ],
          achievement: [
           "1. 上线后统一各项目的样式风格，严格保证了公司 ui 设计标准要求",
           "2. 减少前端重复工作量，极大提升开发效率"
          ]
        },
        {
          title: "KPC即时通讯软件",
          timeRange: "（2021.09 - 至今）",
          desc: "项目运用腾讯IM即时通讯服务，自定义消息格式以及公司业务提醒等协议，实现教育培训行业的即时通讯软件。项目包括即时通讯常见的单聊群聊、消息已读未读、群通知以及个人或群信息等功能，还包括公司自己的业务功能。为集团一千多人提供工作沟通等服务。",
          technology: "Vue.js、Electron、Node.js、SQLite",
          duty: [
            "1. 主导负责前端项目的整体进度；",
            "2. 根据技术栈结合腾讯IM即时通讯服务搭建项目的基础项目框架",
            "3. 负责协商定义 Electron 主进程与渲染进程的通讯协议",
            "4. 负责开发前端项目页面渲染交互功能以及与node端和腾讯IM服务对接工作",
            "5. 负责项目所需通用组件的开发",
            "6. 负责项目与其他业务系统的对接引入"
          ],
          achievement: [
           "1. 项目更新迭代更加便捷，更易维护",
           "2. 软件打开速度更快，大大降低了软件占用电脑内存"
          ]
        }
      // ,{
      //   title: "杨梅红线上画院",
      //   timeRange: "（2021.03 - 2021.06）",
      //   desc: "项目采用Vue全家桶以及 turn.js 插件等技术，为了应对当前线下办学的局限性以及为了应对此次机遇挑战，提供线上办学模式。为线上艺术教育的学生家长提供上课以及保存作品等功能。",
      //   duty:[
      //     "1. 开发面对用户组件 UI 组件（按需、全局、服务）以及业务组件；",
      //     "2. 封装高度复用的模块，供各组件调用；",
      //     "3. 开发带有翻书效果的学生作品集模块；",
      //     "4. 请求拦截器处理，自动开启关闭 loading，toast 提示，跳转路由请求取消；"
      //   ],
      //   link: "https://class.ymm.cn"
      // }
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
      min-width: 64px;
      text-align-last: justify;
      font-weight: 550;
      white-space: nowrap;
    }
    &-duty {
      display: flex;
      margin-bottom: 4px;
    }
    &-technology{
      font-size: 15px;
    }
  }
}
</style>
