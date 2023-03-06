<template>
  <div>
    <h1 class="text-2xl mb-3">{{ product.title }}</h1>
    <p>{{ product.description }}</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})
const { id } = useRoute().params

const { data: product } = await useFetch('https://fakestoreapi.com/products/' + id)
console.log(product);
</script>

<style scoped></style>