<template>
  <section class="py-10">
    <div class="container m-auto px-4 max-w-4xl">
      <!-- info for Features -->
      <div class="text-a text-center">
        <h2 class="font-bold text-4xl lg:text-6xl">You ask? we answer</h2>
      </div>
      <!-- list Features -->
      <div class="mt-16">
        <ul>
          <li v-for="item in listdata" :key="item" @click="OpenBox(item)" class="border border-a rounded-md px-4 py-2 lg:py-3 max-h-full mt-6 lg:mb-4">
            <div class="flex justify-between items-center cursor-pointer">
              <h3 class="text-a font-medium flex items-center lg:text-lg">
                <i class="fi fi-br-list-check text-lg w-[18px] h-[18px] mr-2 relative bottom-[2px]"></i>
                {{ item.title }}</h3>
              <div>
                <i v-if="!item.isOpen" class="fi fi-rr-plus-small text-4xl mt-0 w-9 h-9 list-item text-a"></i>
                <i v-if="item.isOpen" class="fi fi-rr-minus-small text-4xl mt-0 w-9 h-9 list-item text-a"></i>
              </div>
            </div>
            <div class="overflow-hidden transition-all max-h-0 ml-[26px]"
              :class="{ 'max-h-full': item.isOpen, 'py-1': item.isOpen }">
              <p class="text-a font-light text-sm">{{ item.info }}</p>
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