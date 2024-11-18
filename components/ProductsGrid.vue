<!-- components/ProductGrid.vue -->
<template>
    <div class="container mx-auto px-4 py-8">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="product in products" :key="product.id" class="relative group">
          <div class="relative aspect-square overflow-hidden rounded-lg">
            <img 
              :src="product.image" 
              :alt="product.name"
              class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
            />
            <button 
              class="absolute top-4 right-4 p-2 rounded-full bg-white/80 hover:bg-white"
            >
              <svg 
                class="w-5 h-5" 
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path 
                  stroke-linecap="round" 
                  stroke-linejoin="round" 
                  stroke-width="2" 
                  d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
                />
              </svg>
            </button>
          </div>
          <div class="mt-4">
            <h3 class="text-lg font-medium text-gray-900">{{ product.name }}</h3>
            <p class="mt-1 text-orange-500">{{ product.price }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductGrid',
    data() {
      return {
        products: [
          {
            id: 1,
            name: 'Tiramisu Quế Hoa',
            price: '245.000 VND',
            image: '/tiramisu_quehoa.jpg'
          },
          {
            id: 2,
            name: 'Tiramisu Whiskey',
            price: '245.000 VND',
            image: '/tiramisu_whiskey.jpg'
          },
          {
            id: 3,
            name: 'Tiramisu Grappa',
            price: '155.000 VND',
            image: '/grappa.jpg'
          },
          {
            id: 4,
            name: 'Tiramisu Circle',
            price: '555.000 VND',
            image: '/tiramisu_circle.jpg'
          },
          {
            id: 5,
            name: 'Tiramisu Early Grey',
            price: '155.000 VND',
            image: '/EarlGrey_Rhum.jpg'
          },
          {
            id: 6,
            name: 'Avocado CheeseCake',
            price: '555 .000 VND',
            image: '/avocado_ck.jpg'
          }
        ]
      }
    }
  }
  </script>