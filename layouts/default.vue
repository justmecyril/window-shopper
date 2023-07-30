<template>
  <div>
    
    <header class="shadow-md bg-white">
      <nav class="container flex justify-between p-4 mx-auto">
        <NuxtLink to="/" class="font-bold">Window Shopper</NuxtLink>
        <ul class="flex gap-4 ">
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/products" class="btn">Products</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <!-- output the page content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
  </div>
</template>