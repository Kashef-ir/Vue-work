<script setup>
import { defineProps } from "vue";
import { RouterLink, useRoute } from "vue-router";
import logo from "@/assets/img/logo.png";

const route = useRoute();

const isActiveLink = (href) => {
  return route.path === href;
};

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
          <RouterLink class="flex flex-shrink-0 items-center mr-4" to="/">
            <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
            <span class="hidden md:block text-white text-2xl font-bold ml-2"
              >Vue Jobs</span
            >
          </RouterLink>
          <div class="md:ml-auto">
            <div class="flex space-x-2">
              <RouterLink
                v-for="(item, index) in items"
                :key="index"
                :to="item.href"
                :class="[
                  'text-white rounded-md px-3 py-2',
                  isActiveLink(item.href)
                    ? 'bg-green-900 shadow-md'
                    : 'hover:bg-green-900 hover:text-white',
                ]"
              >
                {{ item.label }}
              </RouterLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
