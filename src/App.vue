<script setup>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import HomeCards from "@/components/HomeCards.vue";
import { navbarItems } from "@/data/navbarItems.js";
</script>

<template>
  <Navbar :items="navbarItems" />
  <Hero
    title="Become A Vue Dev"
    subtitle="Find the Vue job that fits your skills and needs"
  />
  <HomeCards />
</template>