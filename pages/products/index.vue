<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products" :key="product.id">
        <!-- <img :src="product.image" alt=""> -->
        <NuxtLink :to="'/products/' + product.id">{{ product.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})

// fetch products
const { data: products } = await useFetch('https://fakestoreapi.com/products')

</script>

<style scoped></style>