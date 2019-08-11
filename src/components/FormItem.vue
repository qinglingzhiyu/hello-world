<!--
 * @Author: Terris
 * @Github: https://github.com/qinglingzhiyu
 * @Date: 2019-08-11 14:27:25
 * @LastEditors: Terris
 * @LastEditTime: 2019-08-11 17:13:49
 * @Description: 这是表单项组件
 -->
<template>
  <div>
    <label v-if="label">{{label}}</label>
    <div>
      <solt></solt>
      <!-- 验证错误信息 -->
      <p v-if="validateStatus == 'error'" class="error">{{errorMessage}}</p>
    </div>
  </div>
</template>

<script>
export default {
  inject: ['form'],
  props: ['label', 'prop'],
  data() {
    return {
      validateStatus: '',
      errorMessage: ''
    }
  },
}
</script>

<style scoped>
  .error{
    color: #f00;
  } 
</style>
