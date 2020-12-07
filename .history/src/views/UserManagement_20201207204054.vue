<!--
 * @Description: 
 * @Github: git@codeup.aliyun.com:5e9ad1c5e17c0e0001fd8d5b/WMS3RD/FE/Tolstoy.git
 * @Date: 2020-12-07 19:19:57
 * @LastEditTime: 2020-12-07 20:40:53
-->
<template>
  <div class="user_manage_container">
    <el-input
      v-model="usercontent"
      placeholder="请输入内容"
    ></el-input>
    <el-divider></el-divider>
    <el-button
      type="primary"
      round
      @click="open"
    >跳转</el-button>
  </div>
</template>
 
<script>
import bus from "../util/bus";

export default {
  name: "UserManagement",
  props: {
    // content:[String,Number]
  },
  data() {
    return {
      usercontent: "",
    };
  },
  mounted() {
    // this.usercontent = content;
  },
  methods: {
    open() {
      this.$confirm("是否要离开当前页面？", "提示", {
        confirmButtonText: "确定",
        cancelButtonText: "取消",
        type: "warning",
      })
        .then(() => {
          this.trans();
        })
        .catch(() => {
          this.$message({
            type: "info",
            message: "已取消",
          });
        });
    },
    trans() {
      bus.$emit("trans", this.usercontent);
      bus.$emit("active", 'config-management')
    },
  },
};
</script>
 
<style scoped lang = "sass">
</style>