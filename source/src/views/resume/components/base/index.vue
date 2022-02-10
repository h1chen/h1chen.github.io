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

    <p class="base__work">
      <strong >工作年限：</strong>
      <span class="base__work-text">三年</span>

      <strong >求职意愿：</strong>
      <span class="base__work-text">前端开发</span>
    </p>

    <p class="base__connect">
      <strong>电话|微信：</strong>
      <span class="base__connect-text">13622450494</span>

      <strong>QQ：</strong>
      <span class="base__connect-text">1029267498</span>

      <strong>邮箱：</strong>
      <span class="base__connect-text">1029267498@qq.com</span>
    </p>
  </div>
</template>
<script>
export default {
  name: "base",
  components: {},
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
<style scoped lang="scss">
.base{
  &__info{
    & > span{
      margin-right: 15px;
    } 
  }

  &__work{
    &-text{
      margin-right: 30px;
    }
  }

  &__connect{
    &-text{
      margin-right: 20px;
    }
  }
}
</style>
