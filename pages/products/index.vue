<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products" :key="product.id">
        <NuxtLink :to="'/products/' + product.slug">{{ product.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})

// fetch products
const result = await useFetch('https://api.storerestapi.com/products')
const products = result.data._rawValue.data
console.log(products);
</script>

<style scoped></style>