<script setup lang="ts">
import { defineProps, type PropType } from 'vue';

type navItem = {
  title: string,
  route?: string,
  icon: any,
  selected: boolean
}

defineProps({
  item: {
    type: Object as PropType<navItem>,
    required: true
  },
  isSelected: {
    type: Boolean,
    default: false
  }
})


</script>
<template>
  <div
    class="w-fit p-3 text-2xl text-neutral-400 duration-300 cursor-pointer hover:bg-zinc-600 hover:bg-opacity-25 rounded-3xl"
  >
    <div :class="['flex items-center gap-2', item.selected ? 'text-neutral-50' : '']">
      <div class="h-8 w-8">
        <slot></slot>
      </div>
      <div>{{ item.title }}</div>
    </div>
  </div>
</template>