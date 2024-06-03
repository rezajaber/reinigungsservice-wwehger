<script setup lang="ts">
import Header from '../components/Header.vue'
import NavBar from '../components/NavBar.vue'
import Hero from '../components/Hero.vue'
</script>

<template>
  <div>
    <Header class="bg-header h-[88px]" />
    <NavBar class="fixed inset-x-0 z-10 -mt-[45px]" />
    <Hero />
  </div>
</template>
