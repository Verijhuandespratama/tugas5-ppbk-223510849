<script setup>
import Navbar from './components/Navbar.vue'
import Carousel from './components/Carousel.vue'
import Card from './components/Card.vue'
import Footer from './components/Footer.vue'
import { ref } from 'vue';

const products = ref([
  { id: 1, name: 'Repsol', price: 'Rp60.000.000', image: 'https://th.bing.com/th/id/OIP.VhBOiVSTdurbwYkIKIyCjwHaEK?w=285&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7' },
  { id: 2, name: 'Ninja', price: 'Rp54.000.000', image: 'https://th.bing.com/th/id/OIP.9zfgfqlUSmJ523v985SRLgHaEo?w=318&h=197&c=7&r=0&o=5&dpr=1.3&pid=1.7'},
  // Tambahkan lebih banyak produk sesuai kebutuhan
]);
</script>

<template>
  <div id="app">
    <Navbar />
    <Carousel />
    <div class="product-container">
      <Card v-for="product in products" :key="product.id" :product="product" />
    </div>
    <Footer />
  </div>
</template>

<style>
#app {
  font-family: 'Arial', sans-serif;
}
.product-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 20px;
}
</style>