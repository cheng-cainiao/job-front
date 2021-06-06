<template>
  <el-aside width="200px" >
      <div class="logo">
          <img src="../assets/logo.png"/>
          就业招聘网
      </div>
    <el-menu  default-active="2" background-color="#22262E" text-color="#ffffff" active-text-color="#1AA094" >
      <el-menu-item index="1-1"><i class="el-icon-menu"></i></el-menu-item>
      <el-menu-item index="1-2"><i class="el-icon-menu"></i></el-menu-item>
      <el-menu-item index="1-3"><i class="el-icon-menu"></i></el-menu-item>
      <el-menu-item index="1-4"><i class="el-icon-menu"></i></el-menu-item>
    </el-menu>
  </el-aside>
</template>

<script>
export default {
  name: "sidebar"
}
</script>

<style scoped>
   .el-aside{
     background-color: #22262E;
   }

   .logo{
     height:68px;
     width:200px;
     line-height: 60px;
     color: #ffffff;
     font-size: 18px;
     font-weight: 700;
     padding-left: 65px;
     box-sizing: border-box;
   }

   .logo img{
     position: absolute;
     width:45px;
     height:45px;
     left:10px;
     top:7px;

   }
</style>