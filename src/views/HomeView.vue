<script setup>
import Hero from "@/components/Hero.vue";
import HomeCards from "@/components/HomeCards.vue";
import JobListings from "@/components/JobListings.vue";
</script>

<template>
  <Hero
    title="Become A Vue Dev"
    subtitle="Find the Vue job that fits your skills and needs"
  />
  <HomeCards />
  <JobListings :limit="3" :showButton="true" />
</template>
