<!--
 * @Description: 
 * @Github: git@codeup.aliyun.com:5e9ad1c5e17c0e0001fd8d5b/WMS3RD/FE/Tolstoy.git
 * @Date: 2020-12-07 09:19:52
 * @LastEditTime: 2020-12-07 20:09:52
-->
<template>
  <div class="">
    <!-- <A></A> -->
    <Container></Container>
  </div>
</template>
 
<script>
// import A from './A.vue'
import Container from "@/views/Container";

export default {
  name: "Home",
  components: {
    //  A,
    Container,
  },
  data() {
    return {
      msg: "Welcome to your vueName",
    };
  },
  methods: {},
};
</script>
 
<style scoped lang = "sass">
 
</style>