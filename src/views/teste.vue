<script setup>
import back from '@/assets/image/back.jpg'
import Product from '@/components/Cardap.vue';


const products = [
  {
    id: 1,
    name: 'pega o pao caraio',
    image: back,
    rating: 2,
    reviews: 1,
    oldPrice: 229.99, 
    currentPrice: 179.99,
    discount: 21,
    discountText: 'Mais barato no app!',
    installments: '3x de R$ 59,99 sem juros no cartão de crédito',  
  },
];
</script>

<template>
  <div class="product-list">
    <Product v-for="product in products" :key="product.id" :product="product"/>
  </div> 
  </template>


<style scoped>
.product-list {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 16px;
padding: 20px;
}
</style>


