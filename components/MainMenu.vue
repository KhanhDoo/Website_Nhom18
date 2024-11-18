<template>
  <ul id="nm-main-menu-ul" class="nm-menu">
    <!-- Link đến trang Shop -->
    <li
      id="menu-item-2437"
      class="menu-item menu-item-type-post_type menu-item-object-page menu-item-home current-menu-item current_page_item menu-item-2437"
    >
      <NuxtLink to="/" aria-current="page">Shop</NuxtLink>
    </li>
    
    <!-- Link đến trang Giới Thiệu -->
    <li
      id="menu-item-2432"
      class="menu-item menu-item-type-post_type menu-item-object-page menu-item-2432"
    >
      <NuxtLink to="/">Giới Thiệu</NuxtLink>
    </li>
    
    <!-- Link đến trang Giao Hàng -->
    <li
      id="menu-item-2545"
      class="menu-item menu-item-type-post_type menu-item-object-page menu-item-privacy-policy menu-item-2545"
    >
      <NuxtLink to="/">Giao Hàng</NuxtLink>
    </li>
    
    <!-- Link đến trang Thanh Toán -->
    <li
      id="menu-item-2620"
      class="menu-item menu-item-type-post_type menu-item-object-page menu-item-2620"
    >
      <NuxtLink to="/">Thanh Toán</NuxtLink>
    </li>
  </ul>
</template>

<script>
export default {
  name: "MainMenu",
};
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
</style>
