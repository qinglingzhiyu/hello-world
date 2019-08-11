<!--
 * @Author: Terris
 * @Github: https://github.com/qinglingzhiyu
 * @Date: 2019-08-11 16:15:26
 * @LastEditors: Terris
 * @LastEditTime: 2019-08-11 16:52:43
 * @Description: 这是input组件
 -->
<template>
  <div>
    <input :type="type" :value="inputValue" @input="inputHandle">
  </div>
</template>

<script>
export default {
  name: 'Input',
  props:{
    type: {
      type: String,
      default: 'text'
    }
  },
  data () {
    return {
      inputValue: this.value //单向数据流原则：组件内不能修改props属性
    }
  },
  methods: {
    inputHandle: function(e) {
      console.log('e: ', e);
    }
  }
}
</script>

<style>

</style>