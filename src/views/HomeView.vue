<script setup>
import HomeCards from '@/components/HomeCards.vue';
import JobListings from '@/components/JobListings.vue';
import Hero from '@/components/Hero.vue';
</script>

<template>
  <Hero title="Test Title" subtitle="Test Subtitle"/>
  <HomeCards />
  <JobListings :limit="3" :showButton="true"/>
</template>