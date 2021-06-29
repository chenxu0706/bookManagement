<template>
  <el-container>
    <el-header>
      <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b">
        <div class="bookTop">
          <span class="bookTop-1"></span>
          旭日东升图书管理中心
        </div>
        <el-submenu index="1" style="float: right;width: 130px;text-align: center">
          <template style="width: 110px" slot="title">admin</template>
          <el-menu-item style="width: 110px;" index="1-1">个人资料</el-menu-item>
          <el-menu-item style="width: 110px" index="1-2">修改密码</el-menu-item>
        </el-submenu>
      </el-menu>
    </el-header>
    <el-container>
      <el-aside width="210px">
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#ffd04b"
        style="height: 100%">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-set-up"></i>
              <span>权限管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="1-1">配置权限</el-menu-item>
              <el-menu-item index="1-2">修改权限</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-notebook-1"></i>
              <span>图书管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="2-1">书籍信息</el-menu-item>
              <el-menu-item index="2-2">借阅信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-menu-item index="3">
            <i class="el-icon-s-custom"></i>
            <span slot="title">用户管理</span>
          </el-menu-item>
          <el-menu-item index="4">
            <i class="el-icon-setting"></i>
            <span slot="title">系统设置</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>

</template>

<style>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
    padding: 0;

  }

  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    /*text-align: center;*/
    /*line-height: 200px;*/
  }

  .el-main {
    background-color: #E9EEF3;
    color: #333;
    /*text-align: center;*/
    /*line-height: 160px;*/
  }

  body > .el-container {
    /*margin-bottom: 40px;*/

  }
  .el-container{
    width: 100%;
    height: 100%;
  }

  /*修改admin 子菜单*/
  .el-menu--collapse .el-menu .el-submenu, .el-menu--popup{
     min-width: 110px!important;
    text-align: center;
    padding: 0;
  }
  .bookTop{
    float: left;
    font-size: 23px;
    text-align: center;
    font-family: cursive;
    width: 400px;
    display: inline-flex;
    margin-left: 20px;
    height: 60px;
    align-items: center;
    color: #ffffff;
  }
  .bookTop-1{
    width: 40px;
    height: 40px;
    display: block;
    margin-right: 5px;
    background: url("../assets/img/tushu.png") no-repeat;
    background-size: 100% 100%;
  }

</style>

<script>


  export default {
    name: 'home',
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }

  };
</script>
