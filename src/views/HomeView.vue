<script setup lang="ts">
import Header from '../components/Header.vue'
import NavBar from '../components/NavBar.vue'
import Hero from '../components/Hero.vue'
import Vorteile from '../components/Vorteile.vue'
import AboutUs from '../components/AboutUs.vue'
</script>

<template>
  <div>
    <Header class="bg-header h-[88px] px-5 xl:px-0" />
    <NavBar class="fixed inset-x-0 z-50 -mt-[45px] px-5 xl:px-0" />
    <Hero />
    <Vorteile class="my-[120px] px-5 xl:px-0" />
    <AboutUs class="bg-[#f0f4fa] px-5 py-[120px] xl:px-0" />
  </div>
</template>
