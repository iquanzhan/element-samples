<template>
  <el-submenu index="1">
    <template slot="title">
      <i class="el-icon-location"></i>
      <span>导航一</span>
    </template>
    <el-submenu index="1-4">
      <template slot="title">选项4</template>
      <el-menu-item index="1-4-1">选项1</el-menu-item>
    </el-submenu>
  </el-submenu>
</template>

<script>
import SubMenu from "./SubMenu";

export default {
  name: "sub-menu",
  props: ["model"],
  data() {
    return {};
  },
  components: {
      SubMenu
  }
};
</script>

<style scoped>
</style>
