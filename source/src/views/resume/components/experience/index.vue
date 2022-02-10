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
  </div>
</template>

<script>
export default {
  name: "experience",
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
}
</style>
