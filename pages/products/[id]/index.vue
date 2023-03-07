<template>
  <div>
    <h1 class="text-2xl mb-3">{{ product.title }}</h1>
    <p>${{ product.price }}</p>
    <p>{{ product.id }}</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id


// fetch product
const { data: product } = await useFetch(uri)

</script>

<style scoped></style>