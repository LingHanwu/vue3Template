<script setup>

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
        11
      </div>
      <!-- 主体数据 -->
      <div class="main">

      </div>
    </div>


  </div>


</template>

<style lang="less" scoped>
.header {
  height: 60px;
  line-height: 60px;
  background-color: white;

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
  }

  // 主体数据
  .main {
    flex: 1;
    background-color: aqua;
  }
}
</style>
