<template>
  <el-container>
    <el-aside width="200px">
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
      >
        <span v-html="initMenuConfig(this.menuConfig)"></span>
      </el-menu>
    </el-aside>
    <el-container>
      <el-header>Header</el-header>
      <el-main>
        <router-view/>
      </el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</template>

<script>
import menuConfig from "./config/menuConfig.js";

export default {
  name: "App",
  data() {
    return {
      menuConfig: menuConfig
    };
  },
  methods: {
    handleOpen: () => {},
    handleClose: () => {},
    initMenuConfig: config => {
      return (
        config &&
        config.map((item, index) => {
          if (!item.children) {
            return (
              <el-menu-item index={item.key}>
                <i class="el-icon-setting" />
                <span slot="title">{item.title}</span>
              </el-menu-item>
            );
          } else {
            return (
              <el-menu-item-group>
                {this.initMenuConfig(item.children)}
              </el-menu-item-group>
            );
          }
        })
      );
    }
  }
};
</script>

<style>
</style>
