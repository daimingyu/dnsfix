<template>
    <el-tabs :tab-position="tabPosition" stretch>
        <el-tab-pane label="重要域名设置">
			<Domain />
		</el-tab-pane>
        <el-tab-pane label="备用IP池设置">配置管理</el-tab-pane>
    </el-tabs>
</template>
<script>
import Domain from './Domain/Domain';
export default {
	name: 'Setting',
	components: { Domain },
	methods: {} ,
	data() {
		return {
			tabPosition: 'left'
		};
	}
};
</script>
<style>
.el-tabs--left{
  height: 100%;
}
.el-tabs__item{
	text-align: center!important;
}
</style>
