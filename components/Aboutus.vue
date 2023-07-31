<template>
  <section id="aboutus" class="py-28 scroll-mt-2">
    <div class="container m-auto px-4">
      <!-- Goal and vision -->
      <div class="text-a text-center">
        <h2 class="font-bold text-4xl lg:text-6xl">Goal and vision</h2>
        <p class="font-extralight text-sm mt-3 lg:text-lg lg:w-1/2 lg:mt-4 lg:m-auto">Our goal at Tasky is to simplify task management boost productivity,and help
          users achieve their goals effortlessly.</p>
      </div>
      <!-- img & List Goal -->
      <div class="lg:flex lg:justify-center lg:mt-7">
        <div class="mt-5 lg:w-1/2 lg:mt-0 lg:mr-3">
          <img class="rounded-md " src="/assets/img/pexels-andrea-piacquadio-3800497.jpg">
        </div>
        <div class="lg:w-1/2">
          <ul>
            <li v-for="item in listdata" :key="item" @click="OpenBox(item)" class="border border-a rounded-md px-3 py-3 max-h-full mt-4 lg:mt-0 lg:mb-4">
              <div class="flex justify-between items-center cursor-pointer">
                <h3 class="text-a font-medium select-none">{{ item.title }}</h3>
                <div>
                  <i v-if="!item.isOpen" class="fi fi-rr-angle-small-down text-3xl mt-0 w-[30px] h-[30px] list-item text-a"></i>
                  <i v-if="item.isOpen" class="fi fi-rr-angle-small-up text-3xl mt-0 w-[30px] h-[30px] list-item text-a"></i>
                </div>
              </div>
              <div class="overflow-hidden max-h-0 transition-all duration-300"
                :class="{ 'max-h-[500px]': item.isOpen }">
                <p class="text-a font-extralight text-sm mb-2">{{ item.info }}</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <!-- vision -->
      <div class="font-extralight text-a text-center mt-5 text-xs lg:text-lg lg:w-1/2 lg:m-auto lg:mt-7">
        <p>
          Our vision is to revolutionize task management and productivity by
          providing a user-friendly app that simplifies lives and empowers 
          users to achieve more.
        </p>
      </div>
      <div class="text-center mt-10">
        <NuxtLink class="text-a text-lg border border-a py-3 px-6 rounded-md hover:bg-a hover:text-white transition-all" to="#">About us</NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
const  data  = await useAsyncData(() => queryContent('/api/goalvision').findOne())

</script>

<script>
export default {
  data() {
    return {
      listdata: [
        { title: "Streamlined Task Management", info: "Our app aims to offer a streamlined and intuitive platform for managing tasks, projects, and deadlines. Users can easily create, assign, and track tasks, ensuring efficient task management.", isOpen: false },
        { title: "Streamlined Task Management", info: "Our app aims to offer a streamlined and intuitive platform for managing tasks, projects, and deadlines. Users can easily create, assign, and track tasks, ensuring efficient task management.", isOpen: false },
        { title: "Streamlined Task Management", info: "Our app aims to offer a streamlined and intuitive platform for managing tasks, projects, and deadlines. Users can easily create, assign, and track tasks, ensuring efficient task management.", isOpen: false },
        { title: "Streamlined Task Management", info: "Our app aims to offer a streamlined and intuitive platform for managing tasks, projects, and deadlines. Users can easily create, assign, and track tasks, ensuring efficient task management.", isOpen: false },
      ]
    }
  },
  methods: {
    OpenBox(item) {
      item.isOpen = !item.isOpen;
    }
  }
}
</script>