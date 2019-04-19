<template>
  <div>
    <el-menu @open="handleOpen" @close="handleClose">

      <el-menu-item index="1-4-1">选项1</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
import menuConfig from "./../config/menuConfig.js";
import SubMenu from "./SubMenu";

export default {
  name: "TreeMenu",
  data() {
    return {
      treeData: menuConfig
    };
  },
  components: {
    SubMenu
  },
  methods: {
    handleOpen() {},
    handleClose() {}
  },
  computed: {
      isSubMenu(){
          return 
      }
  }
};
</script>

<style scoped>
</style>
