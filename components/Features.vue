<template>
  <section id="features" class="py-28 scroll-mt-2">
    <div class="container m-auto px-4">
      <!-- info for Features -->
      <div class="text-a text-center">
        <h2 class="font-bold text-4xl lg:text-6xl">Key Features</h2>
        <p class="font-extralight text-sm mt-3 lg:text-lg lg:w-1/2 lg:mt-4 lg:m-auto">Discover the power of our app's key features, designed to revolutionize your task management and boost your productivity</p>
      </div>
      <!-- list Features -->
      <div class="lg:mt-6">
        <ul class="lg:grid lg:grid-cols-2 lg:gap-6">
          <li v-for="item in listdata" :key="item"
            class="border border-a rounded-md px-5 py-[18px] max-h-full mt-6 lg:mt-0">
            <div class="flex justify-between items-center cursor-pointer">
              <h3 class="text-a font-medium flex items-center text-lg">
                <i class="fi fi-br-list-check text-lg w-[18px] h-[18px] mr-2 relative bottom-[2px]"></i>
                {{ item.title }}
              </h3>
            </div>
            <div class="ml-[26px] mt-[2px]">
              <p class="text-a font-extralight text-sm">{{ item.info }}</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      listdata: [
        { title: "Streamlined Task Management", info: "Effortlessly manage tasks, projects, and deadlines with our streamlined task management feature." },
        { title: "Streamlined Task Management", info: "Effortlessly manage tasks, projects, and deadlines with our streamlined task management feature." },
        { title: "Streamlined Task Management", info: "Effortlessly manage tasks, projects, and deadlines with our streamlined task management feature." },
        { title: "Streamlined Task Management", info: "Effortlessly manage tasks, projects, and deadlines with our streamlined task management feature." },
        
      ]
    }
  },
}
</script>
