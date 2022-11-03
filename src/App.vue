<script setup lang="ts">
import { ref } from 'vue'
</script>

<template>

  <div>
    <!-- 头部区域 -->
    <nav class="header">
      <span class="title">图书管理系统</span>
    </nav>

    <!-- 侧边栏和主体 -->
    <div class="container">
      <!-- 侧边栏导航 -->
      <div class="slider">
        <el-menu default-active="$router.path" class="el-menu-vertical-demo" router>
          <el-menu-item index="home">
            <template #title>首页</template>
          </el-menu-item>
          <el-sub-menu index="1">
            <template #title>
              <span>关于页面</span>
            </template>
            <el-menu-item index="about">关于详情</el-menu-item>
          </el-sub-menu>
        </el-menu>
      </div>
      <!-- 主体数据 -->
      <div class="main">
        <router-view></router-view>
      </div>
    </div>


  </div>


</template>

<style lang="less" scoped>
.header {
  height: 60px;
  line-height: 60px;
  background-color: #5bd896;

  .title {
    margin: 25px;
    font-size: 24px;
  }
}

.container {
  display: flex;

  // 侧边栏
  .slider {
    width: 200px;
    height: calc(100vh - 60px);
    overflow: hidden;
    margin-right: 2px;
    background-color: white;
    min-width: 200px;
  }

  // 主体数据
  .main {
    flex: 1;
    background-color: white;
  }
}
</style>
