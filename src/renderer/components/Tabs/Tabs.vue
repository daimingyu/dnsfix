<template>
  <el-tabs v-model="activeName" @tab-click="handleClick" stretch>
    <el-tab-pane label="使用说明" name="readme"> 
        <Readme /> 
    </el-tab-pane>
    <el-tab-pane label="DNS健康状态检测" name="check">
        <Check />
    </el-tab-pane>
    <el-tab-pane label="公共DNS配置" name="dnsFix">公共DNS配置</el-tab-pane>
    <el-tab-pane label="HOST修复" name="hostFix">HOST修复</el-tab-pane>
    <el-tab-pane label="管理员设置" name="setting">
        <Setting />
    </el-tab-pane>
  </el-tabs>
</template>
<script>
  import Readme from '../Readme/Readme';
  import Check from '../Check/Check';
  import Setting from '../Setting/Setting';
  export default {
    components: { Readme, Check, Setting },
    data() {
      return {
        activeName: 'readme'
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>
<style>
.el-tabs--top{
    flex:1;
    display: flex;
    flex-direction: column;
}
.el-tabs__content,.el-tab-pane{
    height: 100%;
}
</style>
