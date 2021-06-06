<template>
  <el-header>
    <span class="collapse">
      <i class="el-icon-s-fold"></i>
    </span>
    <div class="user-info">
      <i class="el-icon-chat-line-square"></i>
      <i class="el-icon-full-screen"></i>
          <el-dropdown @command="handleCommand">
              <span class="el-dropdown-link">
                admin<i class="el-icon-caret-bottom el-icon--right"></i>
              </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>个人信息</el-dropdown-item>
              <el-dropdown-item>修改密码</el-dropdown-item>
              <el-dropdown-item>退出登录</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
    </div>
  </el-header>
</template>

<script>
export default {
  name: "Navbar",
  methods:{
    handleCommand(type){
      console.log(type)
      if(type === 'logout'){
        this.$confirm('确定要退出吗？','退出提示',).then(()=>{
          this.$router.push('/login');
        }).catch(()=>{});
      }
      if(type === 'home'){
        this.$router.push('/');
      }
    }
  }
}



</script>

<style scoped>
  .el-header{
    height: 60px;
    background-color: #1AA094;
    width:100%;
    padding: 0px;
    line-height: 60px;
    display: flex;
  }

  .collapse{
    cursor: pointer;
    padding: 0px 20px;
    color: #ffffff;
  }

  .user-info{
    height: 60px;
    margin-left: auto;
    padding-right: 20px;
    width:400px;
    text-align: right;
  }

  .user-info>i{
    cursor: pointer;
    padding: 10px 15px;
  }

  .el-dropdown-link{
    color: #ffffff;
    cursor: pointer;
  }


</style>