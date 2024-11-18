<!-- components/NavigationMenu.vue -->
<template>
    <nav class="flex items-center gap-6 p-4 border-b">
      <router-link 
        v-for="item in menuItems" 
        :key="item.id"
        :to="item.path"
        :class="[
          'text-gray-700 hover:text-orange-500 transition-colors',
          { 'text-orange-500': item.id === 'all' }
        ]"
      >
        {{ item.label }}<span> / </span>
      </router-link>
  
      <div class="ml-auto flex items-center gap-4">
        <button class="text-gray-700 hover:text-gray-900">
          Lọc
        </button>
        
        <div class="relative">
          <input 
            type="search"
            placeholder="Tìm kiếm"
            class="pl-3 pr-8 py-1 border rounded-md focus:outline-none focus:ring-1 focus:ring-orange-500"
          />
          <span class="absolute right-2 top-1/2 -translate-y-1/2">
            🔍
          </span>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NavigationMenu',
    data() {
      return {
        menuItems: [
          { id: 'all', label: 'All ', path: '/'},
          { id: 'best-seller', label: 'Bán Chạy Nhất', path: '/'},
          { id: 'must-try', label: 'Phải Thử', path: '/' },
          { id: 'new', label: 'Sản Phẩm Mới', path: '/' },
          { id: 'hot', label: 'Đang Hot', path: '/' },
        ]
      }
    }
  }
  </script>