<template>
  <Logo/>
  <MainMenu/>
  <div class="login-container">
    <div class="login-box">
      <h2>Đăng nhập</h2>
      <form @submit.prevent="handleSubmit">
        <div class="form-group">
          <label for="email">Tên tài khoản hoặc địa chỉ email *</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="password">Mật khẩu *</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <div class="form-group">
          <button type="submit" class="login-btn">Đăng nhập</button>
        </div>
          <button type="button" @click="goToForgotPassword">Quên mật khẩu?</button>
      </form>
      <p class="signup-link">Chưa có tài khoản?<a href="/register">   Vui lòng đăng ký</a></p>
    </div>
  </div>
  <Footer/>
 </template>
 

 <script>

 export default {
  name: 'LoginPage',
  
  data() {
    return {
      email: '',
      password: '',
      
    }
  },  
  methods: {
    handleSubmit() {
      // Xử lý đăng nhập (API hoặc xác thực)
      console.log("Đăng nhập:", { email: this.email, password: this.password, rememberMe: this.rememberMe });
      alert("Đăng nhập thành công!");
    },
    goToForgotPassword() {
      this.$router.push("/forgot-password");
    },
  },
};
 </script>
 
 <style scoped>
 .login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f5f5f5;
 }
 
 .login-box {
  width: 400px;
  padding: 40px;
  background-color: white;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  border-radius: 5px;
 }
 
 h2 {
  text-align: center;
  margin-bottom: 20px;
 }
 
 .form-group {
  margin-bottom: 20px;
 }

 label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
 }
 
 input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
 }
.remember-me {
  font-size: 14px;
  color: #555;
}
 .login-btn {
  width: 100%;
  padding: 10px;
  background-color: #FFCC59;
  color: white;
  border: none;
  border-radius: 3px;
  cursor: pointer;
 }
 .login-btn:hover{
  color: #CC0E0E;
 }
 .form-group + button {
  background: none;
  border: none;
  color: #007bff;
  text-align: right;
  font-size: 14px;
  padding: 0;
  cursor: pointer;
  display: block;
  width: 100%;
}
.form-group + button:hover {
  text-decoration: underline;
}
 .signup-link {
  text-align: center;
  margin-top: 20px;
 }
 .signup-link a:hover{
  color: #3b9aff;
 }
 </style>