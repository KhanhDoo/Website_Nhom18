<template>
    <Logo/>
    <MainMenu/>
    <div class="register-container">
      <div class="register-box">
        <h2>Đăng ký</h2>
        <form @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="email">Địa chỉ email *</label>
            <input
              type="email"
              id="email"
              v-model="email"
              required
            />
          </div>
          <div class="form-group">
            <label for="password">Mật khẩu *</label>
            <input
              type="password"
              id="password"
              v-model="password"
              required
            />
          </div>
          <div class="form-group">
            <button type="submit" class="register-btn">Đăng ký</button>
          </div>
        </form>
        <p class="login-link">
          Đã có tài khoản?
          <a href="/login">   Đăng nhập</a>
        </p>
      </div>
    </div>
    <Footer/>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: "",
        password: "",
      };
    },
    methods: {
      handleSubmit() {
        console.log("Đăng ký với email:", this.email);
        // Thêm logic xử lý đăng ký
      },
    },
  };
  </script>
  
  <style scoped>
  .register-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f9f9f9;
  }
  
  .register-box {
    width: 400px;
    padding: 20px;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .register-box h2 {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .form-group {
    margin-bottom: 15px;
  }
  
  .form-group label {
    display: block;
    margin-bottom: 5px;
  }
  
  .form-group input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  .register-btn {
    width: 100%;
    padding: 10px;
    background-color: #FFCC59;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .register-btn:hover {
    color: #CC0E0E;
  }
  
  .login-link {
    text-align: center;
    margin-top: 10px;
  }
  
  .login-link a {
    color: #00509e;
    text-decoration: none;
  }
  
  .login-link a:hover {
    text-decoration: underline;
  }
  </style>
  