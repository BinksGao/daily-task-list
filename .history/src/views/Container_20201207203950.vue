<!--
 * @Description: 
 * @Github: git@codeup.aliyun.com:5e9ad1c5e17c0e0001fd8d5b/WMS3RD/FE/Tolstoy.git
 * @Date: 2020-12-07 19:24:58
 * @LastEditTime: 2020-12-07 20:39:50
-->
<template>
  <!-- 2020-12-07 第一个任务后续 -->
  <!-- 这是上次的需求：两个页面A、B，A页面有输入框，在A页面跳转到B页面时，提示用户是否要离开当前页面，并保存输入框的内容，由B页面切换到A页面时，输入框内容仍然存在。 -->
  <!-- 因为理解不同所以现在重新开始做。真正想要的是：同一个页面两个tab切换传值 -->
  <!-- @userTrans="containerFn" :content="containerValue" -->

  <div class="container">
    <el-tabs
      v-model="activeName"
      @tab-click="handleClick"
    >
      <el-tab-pane
        label="用户管理"
        name="user-management"
      >
        <user-management></user-management>
      </el-tab-pane>
      <el-tab-pane
        label="配置管理"
        name="config-management"
      >
        <config-management></config-management>
      </el-tab-pane>
    </el-tabs>
  </div>

</template>
 
<script>
import UserManagement from "./UserManagement.vue";
import ConfigManagement from "@/views/ConfigManagement";
export default {
  components: {
    UserManagement,
    ConfigManagement,
  },
  name: "Container",
  props: {},
  data() {
    return {
      activeName: "user-management",
      //  containerValue:''
    };
  },
  methods: {
    handleClick() {},
    //  containerFn(val){
    //    console.log(val,"111111");
    //    this.transValue = val;
    //    this.handleClick();
    //  }
  },
};
</script>
 
<style scoped lang = "sass">
 
</style>