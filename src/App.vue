<script setup lang="ts">
import NavBar from "@/components/Menu/NavBar.vue";

</script>

<template>
  <div class="min-h-screen bg-neutral-200 dark:bg-zinc-800 text-slate-100">
    <div class="flex flex-row min-h-screen max-w-[90rem] mx-auto">
      <div class="w-1/5 min-w-fit mx-auto">
        <NavBar />
      </div>

      <div class="flex-1">
        <div class="h-40">content</div>
        <div class="h-40">content</div>
        <div class="h-40">content</div>
        <div class="h-40">content</div>
        <div class="h-40">content</div>
        <div class="h-40">content</div>
        <div class="h-40">content</div>
      </div>
    </div>
  </div>

  <!-- <RouterView /> -->
</template>

<style>
.header-h {
  height: 2.75rem;
}

.custom-h-full {
  min-height: calc(100vh - 2.75rem);
  height: calc(100vh - 2.75rem);
}
/* @import "@/assets/base.css"; */
</style>
