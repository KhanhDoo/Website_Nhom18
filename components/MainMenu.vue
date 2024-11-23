<template>
  <ul id="nm-main-menu-ul" class="nm-menu">
    <!-- Link đến trang Shop -->
    <li
      id="menu-item-1"
      class="menu-item menu-1">
      <NuxtLink to="/" aria-current="page">Shop</NuxtLink>
    </li>
    
    <!-- Link đến trang Giới Thiệu -->
    <li
      id="menu-item-2"
      class="menu-item menu-2">
      <NuxtLink to="/">Giới Thiệu</NuxtLink>
    </li>
    
    <!-- Link đến trang Giao Hàng -->
    <li
      id="menu-item-3"
      class="menu-item menu-3">
      <NuxtLink to="/">Giao Hàng</NuxtLink>
    </li>
    
    <!-- Link đến trang Tài khoản -->
    <li
      id="menu-item-4"
      class="menu-item menu-4">
      <NuxtLink to="/login" class="account-link">Tài Khoản</NuxtLink>
    </li>

    <!-- Link đến trang Thanh Toán -->
    <li
      id="menu-item-5"
      class="menu-item menu-5">
      <NuxtLink to="/">Thanh Toán</NuxtLink>
    </li>
  </ul>
</template>

<script>
export default {
  name: "MainMenu",
 
};
definePageMeta({
  layout: 'default',
  
})
</script>

<style scoped>
.nm-menu {
  display: flex;
  justify-content: center;
  gap: 60px; /* Khoảng cách giữa các mục menu */
  list-style: none;
  padding: 0;
  margin: 0;
}

/* Style cho từng mục menu */
.nm-menu li {
  font-size: 16px;
  font-weight: bold;
}

.nm-menu a {
  color: #333; /* Màu chữ */
  text-decoration: none;
}

.nm-menu a:hover {
  color: #007bff; /* Màu khi hover */
}



/* Style riêng cho mục Tài Khoản */
.account-link {
  color: blue;
  text-decoration: underline;
  cursor: pointer;
  margin-right: 20px;
}
</style>
