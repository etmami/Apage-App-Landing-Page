<template>
  <header class="">

    <!-- desktop -->
    <!-- <section class="h-24 flex items-center justify-between container mx-auto px-4 lg:px-0">
      <div class="logo">
        <img class="w-16" src="~assets/img/logoaage.png">
      </div>
      <nav>
        <ul class="flex text-basic font-medium">
          <li><NuxtLink to="#">Home</NuxtLink></li>
          <li><NuxtLink to="#">About us</NuxtLink></li>
          <li><NuxtLink to="#">Features</NuxtLink></li>
          <li><NuxtLink to="#">FaQ</NuxtLink></li>
        </ul>
      </nav>
      <NuxtLink to="#">Download</NuxtLink>
    </section> -->
  
    <!-- phone -->
    <section class="h-24 flex items-center justify-between container mx-auto px-4 lg:px-0">
      <div class="flex justify-between items-center w-full">
        <div class="logo">
          <img class="w-16" src="~assets/img/logoaage.png">
        </div>
        <div>
          <Bar/>
        </div>
      </div>
      <div class="absolute top-24 left-0 right-0 w-full text-center">
        <nav>
          <ul class="text-basic font-medium">
            <li><NuxtLink class="w-full" to="#">Home</NuxtLink></li>
            <li><NuxtLink to="#">About us</NuxtLink></li>
            <li><NuxtLink to="#">Features</NuxtLink></li>
            <li><NuxtLink to="#">FaQ</NuxtLink></li>
          </ul>
        </nav>
        <NuxtLink to="#">Download</NuxtLink>
      </div>
    </section>
  </header>
</template>

<script setup>
  import Bar from '../assets/icons/bars-solid.svg'
</script>

<style scoped>

</style>