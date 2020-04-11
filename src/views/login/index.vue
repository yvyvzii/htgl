<template>
    <div class="login">
      <el-card class="login-cread">
        <div class="tu">
          <img src="../../assets/img/keai.gif" alt="" class="photo">
        </div>
        <!-- 表单 -->
        <el-form :model="loginfrom" :rules="loginrules">
          <el-form-item prop="phono">
              <el-input v-model="loginfrom.phono" placeholder="手机号"></el-input>
          </el-form-item>
          <el-form-item prop="niu">
              <el-input v-model="loginfrom.niu" placeholder="验证码" style="width:60%"></el-input>
              <el-button style="float:right" plain>发送验证码</el-button>
          </el-form-item>
          <el-form-item style="margin-top:-15px" prop="check">
              <el-checkbox v-model="loginfrom.check">必须同意我们欺负你才带你玩</el-checkbox>
          </el-form-item>
          <el-form-item style="margin-top:-15px">
              <el-button type="danger" style="width:100%">主要按钮</el-button>
          </el-form-item>
        </el-form>

      </el-card>
    </div>
</template>

<script>
export default {
  // name: 'login'
  data () {
    return {
      loginfrom: {
        phono: '', // 手机号
        niu: '', // 验证码
        check: false // 复选框
      },
      loginrules: {

      }
    }
  }
}
</script>

<style scoped lang="less">
.login{
  background-image: url("../../assets/img/gugong1.jpg");
  height: 100vh;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  .login-cread{
    width: 440px;
    height: 350px;

  }
}
.tu{
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  .photo{
  width: 130px;
  height: 100px;

}
}

</style>
