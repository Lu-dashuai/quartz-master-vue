<template>
  <div id="table">
    <el-table :data="tableData" style="width: 100%">
      <el-table-column prop="id" label="id" width="150">
      </el-table-column>
      <el-table-column prop="job_name" label="jobName" width="150">
      </el-table-column>
      <el-table-column prop="cron_expression" label="cron表达式" width="150">
      </el-table-column>
      <el-table-column prop="bean_name" label="类名" width="150">
      </el-table-column>
      <el-table-column prop="method_name" label="默认执行方法" width="150">
      </el-table-column>
      <el-table-column prop="status" label="当前状态" width="150">
      </el-table-column>
      <el-table-column prop="delete_flag" label="是否删除" width="150">
      </el-table-column>
      <el-table-column prop="creator_name" label="创建者" width="150">
      </el-table-column>
      <el-table-column prop="created_time" label="创建时间" width="150">
      </el-table-column>
      <el-table-column prop="updated_time" label="上次更新时间" width="150">
      </el-table-column>
      <el-table-column fixed="right" label="操作" width="150">
        <template slot-scope="scope">
          <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
          <el-button type="text" size="small">编辑</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
  export default {
    methods: {
      handleClick(row) {
        alert(row)
      }
    },
    data() {
      return {
        tableData: []
      }
    }
  }

</script>
