<template>
  <div>
    <h3>Product Detail for {{ id }}</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente nemo maxime corporis error, aperiam repellendus
      fugit facilis porro mollitia molestias!</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})
const { id } = useRoute().params
</script>

<style scoped></style>