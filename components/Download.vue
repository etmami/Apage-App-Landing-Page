<template>
  <section id="download" class="bg-b lg:h-screen lg:flex lg:items-center lg:justify-center scroll-mt-[96px]">
    <div class="px-7 py-32 lg: p-32 lg:container lg:flex lg:justify-center lg:items-center lg:max-w-4xl">
      <div>
        <h1 class="text-a text-center lg:text-left text-6xl lg:text-7xl font-bold">{{ realData.title }}</h1>
        <p class="font-extralight text-a text-center mt-5 lg:text-lg lg:text-left">{{ realData.description }}</p>
        <div class="mt-12 lg:mt-8 lg:flex">
          <a v-if="realData.googlePlayLink === 'null'" :href=realData.googlePlayLink><img class="w-1/2 lg:w-52 mt-3 m-auto lg:mr-3 hidden" src="/assets/icons/googleplay.png"></a>
          <a v-else :href=realData.googlePlayLink><img class="w-1/2 lg:w-52 mt-3 m-auto lg:mr-3" src="/assets/icons/googleplay.png"></a>
          <a v-if="realData.appStoreLink === 'null'" :href=realData.appStoreLink><img class="w-1/2 mt-3 m-auto lg:w-52 hidden" src="/assets/icons/appstore.png"></a>
          <a v-else :href=realData.appStoreLink><img class="w-1/2 mt-3 m-auto lg:w-52" src="/assets/icons/appstore.png"></a>
        </div>
        <div class="mt-20">
          <p class="text-center lg:text-left text-a font-light mt-2 flex justify-center lg:justify-start"><i class="fi fi-ss-star text-f text-lg h-[18px] inline-block mr-1"></i>{{ realData.reviewsDescription }}</p>
        </div>
      </div>
      <div class="hidden lg:block">
        <img class="w-96" src="/assets/img/appimg.png">
      </div>
    </div>
  </section>
</template>

<script setup>
  const data = await useAsyncData(() => queryContent('/api/download').findOne())
  const realData = data.data
</script>

<style scoped>
  /* section{
    height: calc(100vh - 96px);
  } */
</style>