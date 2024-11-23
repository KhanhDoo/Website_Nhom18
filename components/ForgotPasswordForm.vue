<template>
    <form @submit.prevent="handleSubmit">
      <h2>Quên Mật Khẩu</h2>
      <div>
        <label>Email</label>
        <input type="email" v-model="email" required />
      </div>
      <button type="submit">Gửi mã</button>
    </form>
  </template>
  
  <script>
  export default {
    setup() {
      const email = ref("");
  
      const handleSubmit = async () => {
        const response = await fetch("/api/forgot-password", {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify({ email: email.value }),
        });
  
        if (response.ok) {
          alert("Vui lòng kiểm tra email để nhận mã xác minh!");
        } else {
          alert("Đã xảy ra lỗi. Vui lòng thử lại.");
        }
      };
  
      return { email, handleSubmit };
    },
  };
  </script>
  
  <style scoped>
  /* CSS styles */
  </style>
  