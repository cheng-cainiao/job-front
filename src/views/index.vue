<template>
  <el-container class="container">
    <sidebar></sidebar>
    <el-container>
      <Navbar></Navbar>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
  import sidebar from "@/components/sidebar";
  import Navbar from "@/components/Navbar";
  export default {
     name: "login",
     components:{
       sidebar,
       Navbar
     }

}
</script>

<style scoped>
  .container{
    height:100%;
    width: 100%;
  }
</style>