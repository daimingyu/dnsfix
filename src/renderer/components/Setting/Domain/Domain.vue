<template>
    <div id="domain">
        <el-input placeholder="请输入内容" v-model="input" class="input-with-select">        
            <el-button slot="append" icon="el-icon-plus"></el-button>
        </el-input>
        <el-table :data="tableData">
            <el-table-column label="域名" min-width="50%" align="center" >
                <template slot-scope="scope">
                    <span style="margin-left: 10px">{{ scope.row.domain }}</span>
                </template>
            </el-table-column>
            <el-table-column label="操作" min-width="50%" align="center" >
                <template slot-scope="scope">
                    <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
                    <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button>
                </template>
            </el-table-column>
        </el-table>
    </div>
</template>
<script>
  export default {
    name: 'Domain' ,
    data() {
        return {
            input: '',
            tableData: [{
                domain: 'www.58cdn.com'
            }, {
                domain: 'www.58cdn.com'
            }, {
                domain: 'www.58cdn.com'
            }, {
                domain: 'www.58cdn.com'
            }]
        }
    },
    methods: {
      handleEdit(index, row) {
        console.log(index, row);
      },
      handleDelete(index, row) {
        console.log(index, row);
      }
    }
  };
</script>
<style>
.el-table{
    width: 100%; 
    margin-top: 10px; 
    border: 1px solid #ebebeb!important;
}
#domain{
    height: 100%;
    overflow-y: scroll;
    padding: 10px;
}
input , .el-input-group__append{
    border-radius: 0px!important;
}
</style>
