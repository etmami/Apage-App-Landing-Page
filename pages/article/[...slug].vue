<template>
  <section class="max-w-3xl m-auto p-10 lg:mt-10 text-basic prose pink">
    <h1 class="font-semibold text-4xl mb-6">{{ data.title }}</h1>
    <ContentDoc  />
  </section>
</template>

<script setup>
  const { path } = useRoute()

  const { data } = await useAsyncData(`content-${path}`, () => {
    return queryContent().where({ _path: path }).findOne()
  })
</script>

<style scoped>

</style>