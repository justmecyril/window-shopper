<template>
  <div>
    <p>{{ product.title }}</p>
    <p>{{ product.price }}</p>
    <p>{{ product.id }}</p>
    <p>{{ product.description }}</p>
  </div>
</template>
 
<script setup>
definePageMeta({
  layout: "products",
});
const { id } = useRoute().params;
const uri = "https://api.escuelajs.co/api/v1/products/" + id;

// fetch the product
const { data: product } = await useFetch(uri, {key: id});
</script> 

<style  scoped>
</style>