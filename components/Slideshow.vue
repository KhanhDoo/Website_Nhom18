<template>
    <div class="slideshow-container">
      <div class="slides">
        <img :src="images[currentIndex]" alt="Slide show" />
      </div>
      <button class="prev" @click="prevSlide">&#10094;</button>
      <button class="next" @click="nextSlide">&#10095;</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        images: [
          '/tiramisu_velvet.jpg', 
          '/tiramisu_chocolate&sake.jpg',
          
        ],
        currentIndex: 0,
        interval: null
      };
    },
    methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
    },
    startAutoSlide() {
      this.interval = setInterval(() => {
        this.nextSlide();
      },10000); // Chuyển ảnh sau mỗi 3 giây
    },
    stopAutoSlide() {
      clearInterval(this.interval);
    },
  },
  mounted() {
    this.startAutoSlide();
  },
  beforeDestroy() {
    this.stopAutoSlide();
  }
};

  </script>
  
<style scoped>
.slideshow-container {
  position: relative;
  max-width: 400px;
  max-height: 600px;
  margin: auto;
  overflow: hidden;
}

.slide {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 600px;
}

.slide img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

button {
  position: absolute;
  top: 50%;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
  font-size: 18px;
  transform: translateY(-50%);
}

.prev {
  left: 10px;
}

.next {
  right: 10px;
}

</style>