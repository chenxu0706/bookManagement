<template>
  <div class="login-in">
      <div class="login-topic">
        智慧图书管理系统
      </div>
      <div class="login">
        <div class="login-1">
          登录/Login
        </div>
        <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
          <el-form-item class="labelCol" label="用户名" prop="name">
            <el-input></el-input>
          </el-form-item>
          <el-form-item class="labelCol" label="密码" prop="password">
            <el-input></el-input>
          </el-form-item>
          <el-form-item>
            <el-button class="loginbutton" @click="toHome()" type="primary">登录</el-button>
          </el-form-item>
        </el-form>
      </div>
  </div>
</template>

<script>
    export default {
        name: "login",
        data:{},
        methods:{
          toHome:function () {
            this.$router.push({
              path: '/home'
            })
          }
        }
    }
</script>

<style>
    .login-in{
      width: 100%;
      height: 100%;
      background: url("../assets/img/login.png") no-repeat;
      background-size: 100% 100%;
    }
  .login{
    width: 320px;
    height: 400px;
    position: absolute;
    top: 24%;
    left: 72%;
  }
  .login-topic{
    position: absolute;
    left: 37%;
    top: 32%;
    color: white;
    font-family: cursive;
    font-size: 60px;
    letter-spacing: 10px;
  }
  .labelCol .el-form-item__label{
    color:white;
  }
  .login-1{
    color: white;
    margin-left: 148px;
    width: 200px;
    font-size: 21px;
    height: 40px;
    margin-bottom: 19px;
  }
  .loginbutton{
    margin-top: 7px;
    width: 221px;
    border-radius: 35px;
  }
</style>
