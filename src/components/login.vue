<!--  -->
<template>
  <div id='login' class="container">
    <div class="login-wrapper">
      <div class="header">Login</div>
      <div class="form-wrapper">
        <input type="text" name="username" placeholder="username" class="input-item">
        <input type="password" name="password" placeholder="password" class="input-item">
        <button class="btn" @click='login'>Login</button>
      </div>
      <div class="msg">
        Don`t have account? <a href="#">Sign up</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      //这里存放数据
      return {

      };
    },
    methods: {
      login() {
        this.$router.push('/home')
      }
    },
    //生命周期 - 创建完成（可以访问当前this实例）
    created() {

    }
  }

</script>
<style>
 * {
  padding: 0;
  margin: 0;
  font-family: 'Open Sans Light';
  letter-spacing: .05em;
}
.btn{
    border-radius: 15px;
}

html {
  height: 100%;
}

body {
  height: 100%;
  background-image: linear-gradient(to right,#fbc2eb,#a6c1ee);
}



.login-wrapper{
  background-color: #fff;
  width: 250px;
  height: 500px;
  border-radius: 15px;
  padding: 0 50px;
  position: relative;
  left: 50%;
  top: 50%;
  transform: translate(-50%,30%);
}

.login-wrapper .header {
  font-size: 30px;
  font-weight: bold;
  text-align: center;
  line-height: 200px;
}

.login-wrapper .form-wrapper .input-item {
  display: block;
  width: 100%;
  margin-bottom: 20px;
  border: 0;
  padding: 10px;
  border-bottom: 1px solid rgb(128, 125, 125);
  font-size: 15px;
  outline: none;
}

.login-wrapper .form-wrapper .input-item::placeholder {
  text-transform: uppercase;
}

.login-wrapper .form-wrapper .btn {
  text-align: center;
  padding: 10px;
  width: 100%;
  margin-top: 40px;
  background-image: linear-gradient(to right,#a6c1ee,#fbc2eb);
  color: #fff;
}

.login-wrapper .msg {
  text-align: center;
  line-height: 80px;
}

.login-wrapper .msg a {
  text-decoration-line: none;
  color: #a6c1ee;
}
</style>
