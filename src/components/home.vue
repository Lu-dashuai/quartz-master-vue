<template>
  <div id="table">
    <el-table :data="tableData" style="width: 100%">
      <el-table-column prop="id" label="id" width="150">
      </el-table-column>
      <el-table-column prop="jobName" label="jobName" width="150">
      </el-table-column>
      <el-table-column prop="cronExpression" label="cron表达式" width="150">
      </el-table-column>
      <el-table-column prop="beanName" label="类名" width="150">
      </el-table-column>
      <el-table-column prop="methodName" label="默认执行方法" width="150">
      </el-table-column>
      <el-table-column prop="status" label="当前状态" width="150">
      </el-table-column>
      <el-table-column prop="creatorName" label="创建者" width="150">
      </el-table-column>
      <el-table-column prop="createdTime" label="创建时间" width="150">
      </el-table-column>
      <el-table-column prop="updatedTime" label="上次更新时间" width="150">
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
        tableData: [{"id":9,"jobName":"任务01","cronExpression":"0/10 * * * * ?","beanName":"testJob01","methodName":"execute","status":1,"deleteFlag":false,"creatorId":1,"creatorName":"admin","createdTime":"2020-04-14T21:36:07","updatedTime":"2020-04-14T21:38:38"},{"id":10,"jobName":"任务02","cronExpression":"0/3 * * * * ?","beanName":"testJob02","methodName":"execute","status":1,"deleteFlag":false,"creatorId":1,"creatorName":"admin","createdTime":"2020-04-14T21:37:14","updatedTime":"2020-04-14T21:38:38"}]
      }
    }
  }

</script>
