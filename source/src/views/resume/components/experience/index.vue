<!--
/****************************************************************************
所属系统: 简历
所属模块: 工作经历
创建时间: 2022年02月09日 22:15
维护人: 张和潮
***************************************************************************/
-->
<template>
  <div class="experience">
    <h3 class="experience__title">工作经历</h3>

    <div 
      v-for="(item, index) of experienceList"
      class="experience__content"
      :key="index"
    >
      <div>
        <span class="experience__content-label">工作单位：</span>
        <span class="experience__content-text">{{ item.company }}{{item.timeRange}}</span>
      </div>

      <div>
        <span class="experience__content-label">工作职责：</span>
        <span>{{ item.duty }}</span>
      </div>

      <div class="experience__content-desc">
        <span class="experience__content-label">工作描述：</span>
        <div>
          <div v-for="(ele, idx) of item.describe" :key="idx">
            {{ ele }}
          </div> 
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "experience",
  components: {},
  mixins: [],
  data() {
    return {
      experienceList: [{
        company: "杰人软件（深圳）有限公司",
        timeRange: "（2020.08 - 至今）",
        duty: "前端开发",
        describe:[
          "1.负责公司现有项目和新项目的修改调试和迭代工作；",
          "2.与后端开发团队紧密配合，重构公司的后台管理系统；"
        ]
      },{
        company: "广东盛迪嘉电子商务股份有限公司（盛迪嘉支付）",
        timeRange: "（2019.04 - 2020.08）",
        duty: "Web前端开发",
        describe:[
          "1.负责公司现有项目和新项目的修改调试和迭代工作；",
          "2.与后端开发团队紧密配合，重构公司的后台管理系统；"
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
.experience{
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
    &-label{
      font-weight: 550;
    }

    &-desc{
      display: flex;
    }
  }
}
</style>
