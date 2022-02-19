<script setup lang='ts'>
import { reactive } from 'vue';
import NavLink from './NavLink.vue';
import { HomeIcon, ArchiveIcon, BeakerIcon, CubeIcon, CodeIcon, HeartIcon } from "@heroicons/vue/outline"



const items = reactive([
  { title: 'Home', route: '/', icon: HomeIcon, selected: false },
  { title: 'Projects', route: 'projects', icon: ArchiveIcon },
  { title: 'Something Ay', route: '/', icon: BeakerIcon },
  { title: 'Boo', route: '/', icon: CubeIcon },
  { title: 'Boo2', route: '/', icon: CodeIcon },
])

const handleClick = (index: number) => {
  for (let i = 0; i < items.length; i++) {
    items[i].selected = i === index;    
  }
}

</script>

<template>
  <div
    class="h-screen p-3 sticky top-0 left-0 ml-auto max-w-fit flex flex-col gap-3 border-r-2 border-white border-opacity-5"
  >
    <div class="text-4xl">L.A.P</div>
    <nav-link @click="handleClick(i)" v-for="(item, i) in items" :item="item" :key="item.title">
      <component v-if="item.icon" :is="item.icon" />
    </nav-link>

    <div class="fixed flex align-center gap-1 bottom-1  text-center">
      <div>Made with</div>
      <HeartIcon class="h-4 w-4 text-red-400" />
    </div>
  </div>
</template>