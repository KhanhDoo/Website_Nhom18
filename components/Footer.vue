<!-- components/TheFooter.vue -->
<template>
    <footer class="bg-navy  flex items-center">
      <div class="container mx-auto px-4">
        <div class="flex items-center justify-between">
          <!-- Left side navigation -->
          <nav class="flex items-center gap-10">
            <NuxtLink 
              v-for="item in menuItems" 
              :key="item.id"
              :to="item.path"
              class="text-sm hover:text-gray-300 transition-colors"
            >
              {{ item.label }}
            </NuxtLink>
          </nav>
  
          <!-- Copyright text -->
          <div class="text-sm text-center">
            © 2024 by The 350F Group
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'TheFooter',
    data() {
      return {
        menuItems: [
          { id: 'shop', label: 'Shop', path: '/shop' },
          { id: 'about', label: 'Giới Thiệu', path: '/about' },
          { id: 'delivery', label: 'Giao Hàng', path: '/delivery' },
          { id: 'payment', label: 'Thanh Toán', path: '/payment' },
        ],
      }
    }
  }
  </script>
  
  <style scoped>
  .bg-navy {
    color: #CC0E0E;
    background-color: #FFCC59;
    height:70px;
  }
 
  
  </style>