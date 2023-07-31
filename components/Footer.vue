<template>
  <footer class="">
    <section class="flex justify-center items-center py-14 bg-a">
      <div class="text-center w-2/3 lg:w-[450px]">
        <p class="text-white font-extralight text-lg leading-[33px]">
          Experience a unique and effortless way to manage your daily tasks with our innovative task management app.
        </p>
        <NuxtLink class="border py-2 px-6 inline-block bg-white text-a rounded-md mr-2 mt-6" to="#">Download</NuxtLink>
      </div>
    </section>
    <section class="bg-a">
      <section class="flex justify-center items-center container m-auto border-b">
        <div>
          <ul class="flex text-2xl text-white">
            <li v-for="item in socialMedia" :key="item">
              <a :href=item.link>
                <i :class="`h-[30px] block m-6` + ` ` + item.icon"></i>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="container m-auto">
        <div class="text-center lg:flex justify-between py-[22.5px]">
          <p class="font-extralight text-white">Copyright 2023, All Rights Reserved</p>
          <NuxtLink class="font-extralight text-white" to="#">Privacy Policy</NuxtLink>
        </div>
      </section>
    </section>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      socialMedia: [
        { title: "twitter", link: "#", icon: "fi fi-brands-twitter" },
        { title: "twitter", link: "#", icon: "fi fi-brands-facebook" },
        { title: "twitter", link: "#", icon: "fi fi-brands-instagram" },
        { title: "twitter", link: "#", icon: "fi fi-brands-github" },
      ]
    }
  },
}
</script>