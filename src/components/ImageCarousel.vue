<template>
  <div>
    <h1>Image Carousel below </h1>
    <button @click="prevImage"><-</button>
    <button @click="nextImage">-></button>
    <div class="carousel">
      <img :src="images[currentIndex]" alt="Carousel Image" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const images = [
  'https://via.placeholder.com/600x400?text=Image+1',
  'https://via.placeholder.com/600x400?text=Image+2',
  'https://via.placeholder.com/600x400?text=Image+3'
]

const currentIndex = ref(0)

const nextImage = () => {
  currentIndex.value = (currentIndex.value + 1) % images.length
}

const prevImage = () => {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length
}
</script>

<style scoped>
.carousel {
  height: 300px;
}
</style>