<script setup>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";

const navbarItems = [
  { label: "Home", href: "index.html", active: true },
  { label: "Jobs", href: "jobs.html", active: false },
  { label: "Add Job", href: "add-job.html", active: false },
];
</script>

<template>
  <Navbar :items = "navbarItems"/>
  <Hero
    title="Become A Vue Dev"
    subtitle="Find the Vue job that fits your skills and needs"
  />
</template>

<style scoped></style>
