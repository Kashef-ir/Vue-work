<script setup>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import HomeCards from "@/components/HomeCards.vue";
import { navbarItems } from "@/data/navbarItems.js";
import JobListings from "./components/JobListings.vue";
</script>

<template>
  <Navbar :items="navbarItems" />
  <Hero
    title="Become A Vue Dev"
    subtitle="Find the Vue job that fits your skills and needs"
  />
  <HomeCards />
  <JobListings :limit="3" :showButton="true"/>
</template>