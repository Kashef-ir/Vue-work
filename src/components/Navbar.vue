<script setup>
import { defineProps } from "vue";
import logo from "@/assets/img/logo.png";

defineProps({
  items: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <nav class="bg-green-700 border-b border-green-500">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <div
          class="flex flex-1 items-center justify-center md:items-stretch md:justify-start"
        >
          <!-- Logo -->
          <a class="flex flex-shrink-0 items-center mr-4" href="index.html">
            <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
            <span class="hidden md:block text-white text-2xl font-bold ml-2"
              >Vue Jobs</span
            >
          </a>
          <div class="md:ml-auto">
            <div class="flex space-x-2">
              <a
                v-for="(item, index) in items"
                :key="index"
                :href="item.href"
                :class="[
                  'text-white rounded-md px-3 py-2',
                  item.active
                    ? 'bg-green-900 shadow-md'
                    : 'hover:bg-green-900 hover:text-white',
                ]"
              >
                {{ item.label }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
