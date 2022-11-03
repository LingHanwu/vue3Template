<script setup>

</script>

<template>
  <div id="nav">
    <el-button type="primary">Primary</el-button>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view />
</template>

<style lang="less" scoped>

</style>
