<!--
 * @Author: Terris
 * @Github: https://github.com/qinglingzhiyu
 * @Date: 2019-08-11 13:57:18
 * @LastEditors: Terris
 * @LastEditTime: 2019-08-11 17:17:32
 * @Description: 这是表单验证
 -->
<template>
  <div>
    <h3>{{title}}</h3>
    <!-- model数据模型 -->
    <el-form :model="ruleForm" :rules="rules" ref="loginForm">
      <!-- prop用于校验 -->
      <el-form-item label="用户名" prop="name">
        <el-input v-model="ruleForm.name"></el-input>
      </el-form-item>
      <el-form-item label="密码" prop="pwd">
        <el-input v-model="ruleForm.pwd"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="submitForm()">登录</el-button>
      </el-form-item>
    </el-form>

    <!--  -->
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      ruleForm: {
        name: "",
        pwd: ""
      },
      rules: {
        name: [
          { required: true, message: "请输入名称" },
          { min: 6, max: 10, message: "请输入6-10位的用户名" }
        ],
        pwd: [{ required: true, message: "请输入密码" }]
      }
    };
  },
  methods: {
    submitForm() {
      this.$refs.loginForm.validate(valid => {
        if (valid) alert("提交成功!");
        else {
          // eslint-disable-next-line
          console.log("验证失败");
          return false;
        }
      });
    }
  }
};
</script>
<style>
</style>