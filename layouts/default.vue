<template>
  <div>
    <header class="shadow-md bg-white">
      <div class="container flex p-4 mx-auto justify-between">
        <NuxtLink
          to="/"
          class="font-bold bg-gradient-to-r from-pink-500 to-violet-500 text-transparent bg-clip-text"
          >Window Shopper</NuxtLink
        >
        <nav class="flex gap-8">
          <div v-for="m in menu" :key="m.name" class="last:btn">
            <NuxtLink
              :to="m.link"
              :class="[$route.path === m.link ? active : inactive]"
              >{{ m.name }}</NuxtLink
            >
          </div>
        </nav>
      </div>
    </header>
    <!-- output the page content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
  </div>
</template>

<script setup>
const menu = ref([
  { name: "Home", link: "/" },
  { name: "About", link: "/about" },
  { name: "Products", link: "/products" },
]);

const active = "text-red-800";
const inactive = "text-black";
</script>