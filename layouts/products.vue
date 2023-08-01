<template>
  <div>
    <header class="shadow-md bg-white">
      <nav
        class="container p-4 mx-auto bg-gradient-to-r from-pink-500 to-violet-500 text-transparent bg-clip-text"
      >
        <NuxtLink to="/products" class="font-bold">Window Shopper</NuxtLink>
      </nav>
    </header>
    <!-- output the page content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <footer class="container mx-auto p-4 border-t-2">
      <nav class="flex gap-8">
        <div v-for="m in menu" :key="m.name" class="last:btn">
          <NuxtLink
            :to="m.link"
            :class="[$route.path === m.link ? active : inactive]"
            >{{ m.name }}</NuxtLink
          >
        </div>
      </nav>
    </footer>
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