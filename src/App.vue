<script setup>
import Navbar from "@/components/Navbar.vue";
import { navbarItems } from "@/data/navbarItems.js";
import { RouterView } from "vue-router";
</script>

<template>
  <Navbar :items="navbarItems" />
  <RouterView />
</template>