<script setup>
import { onMounted, ref } from 'vue'
// 输入框数据
const input = ref('')
// 表格数据
const tableData = []

const load = () => {
  fetch('http://localhost:8080/user/list').then(res => res.json()).then(
    res => {
      console.log(res)
      this.tableData = res
    }
  )
}

onMounted(() => {
  load()
})

</script>

<template>
  <div class="home">
    <!-- 搜索框 -->
    <div class="input">
      <el-input style="width:240px" v-model="input" placeholder="请输入名称" />
      <el-input style="width:240px;margin-left:5px;" v-model="input" placeholder="请输入联系方式" />
      <el-button style="margin-left:5px;" type="primary">搜索</el-button>
    </div>
    <!-- 表格数据 -->
    <el-table :data="tableData" style="width: 100%">
      <el-table-column prop="name" label="名称" width="180" />
      <el-table-column prop="age" label="年龄" width="180" />
      <el-table-column prop="address" label="地址" width="180" />
      <el-table-column prop="phone" label="联系方式" />
      <el-table-column prop="sex" label="男" />
    </el-table>
    <!-- 分页 -->
    <div class="pagination">
      <el-pagination background layout="prev, pager, next" :total="500" />
    </div>


  </div>
</template>

<style lang="less" scoped>
.home {
  margin: 20px;

  .input {
    margin: 20px 0;
  }

  // 分页
  .pagination {
    margin-top: 20px;
  }
}
</style>
