<template>
  <div class="card text-center">
    <img
      :src="product.image"
      alt="product thumb"
      class="thumb max-h-[120px] max-w-prose mx-auto my-0"
    />
    <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>

    <NuxtLink :to="`/products/${product.id}`" v-if="$route.path !== '/'">
      <p class="btn my-4">View Details</p>
    </NuxtLink>
  </div>
</template>

<script setup >
const { product } = defineProps(["product"]);
</script>
