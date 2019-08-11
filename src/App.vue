<!--
 * @Author: Terris
 * @Github: https://github.com/qinglingzhiyu
 * @Date: 2019-08-07 17:33:14
 * @LastEditors: Terris
 * @LastEditTime: 2019-08-11 16:31:09
 * @Description: 
 -->
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <el-button>el-button</el-button>
    </div>
    <!-- form test -->
    <form-test :title="title"></form-test>
  </div>
</template>

<script>
import FormTest from './components/Formtest';
export default {
  name: 'app',
  components: {
    FormTest
  },
  data () {
    return {
      title: '自定义组件'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
