<template>
  <div>
    <Header />
    <main>
      <slot />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~~/components/Footer.vue';

  const components = {
    Header, 
    Footer
  }
</script>

<style>
  *{
    font-family: 'Inter', sans-serif;
  }
  img{
    pointer-events: none;
  }
  .nuxt-icon--fill, .nuxt-icon--fill * {
    fill: none !important;
  }
  .nuxt-icon{
    margin-bottom: 0;
  }
</style>