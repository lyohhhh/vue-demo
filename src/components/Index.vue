<template>
  <div>
      <el-container>
        <el-aside width="200px">
          <el-menu router
              default-active="2"
              class="el-menu-vertical-demo">
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-location"></i>
                  <span>导航一</span>
                </template>
                <el-menu-item index="/index">选项1</el-menu-item>
                <el-menu-item index="1-2">选项2</el-menu-item>
              </el-submenu>
              <el-menu-item index="/application">
                <i class="el-icon-menu"></i>
                <span slot="title">应用管理</span>
              </el-menu-item>
              <el-menu-item index="/config">
                <i class="el-icon-document"></i>
                <span slot="title">配置管理</span>
              </el-menu-item>
              <el-submenu index="4">
                <template slot="title">
                  <i class="el-icon-location"></i>
                  <span>导航四</span>
                </template>
                <el-menu-item index="4-1">选项1</el-menu-item>
                <el-menu-item index="4-2">选项2</el-menu-item>
              </el-submenu>
            </el-menu>
        </el-aside>
        <el-container>
            <el-header>{{msg}}</el-header>
            <el-main>
               <router-view/> 
            </el-main>
        </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome 金渡教育'
    }
  },
  methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
