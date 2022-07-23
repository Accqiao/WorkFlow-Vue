<template>
  <el-container>
    <el-aside width="200px">
      <MenuLeft/>
    </el-aside>
    <el-container>
      <el-header>
        Top
      </el-header>
      <BreadCrumb />
      <el-main>
        <router-view></router-view>
      </el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</template>

<script lang='ts' setup>
import MenuLeft from './MenuLeft.vue'
import BreadCrumb from './BreadCrumb.vue'
import { ArrowRight } from '@element-plus/icons-vue'
</script>

<style scoped>
.el-container {
  height: 100%;
}
.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
}
.el-header, .el-footer {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  min-height: 60px;
}
.el-main {
  background-color: #ffffff;
  /* color: #333; */
  /* text-align: center; */
  /* line-height: 160px; */
}

</style>
