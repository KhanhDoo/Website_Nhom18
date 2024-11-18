<template>
    <div class="logo">
      <!-- Banner messages -->
      <img src="/Logo.jpg" alt="Logo" />
    </div>
  </template>
  
<style scoped>
/* Đảm bảo rằng hình ảnh nền phủ toàn bộ */
.logo {
display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;  /* Chiều rộng cố định của container */
  height: 100px;
  background-color:  #ffcc59;
  width: auto;
}
img {
  max-width: 100px;
  max-height: 100px;
}
</style>