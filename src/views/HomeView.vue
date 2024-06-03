<script setup lang="ts">
import Header from '../components/Header.vue'
import NavBar from '../components/NavBar.vue'
import Hero from '../components/Hero.vue'
import Vorteile from '../components/Vorteile.vue'
</script>

<template>
  <div>
    <Header class="bg-header h-[88px] px-5 xl:px-0" />
    <NavBar class="xl-0 fixed inset-x-0 z-10 -mt-[45px] px-5" />
    <Hero />
    <Vorteile class="my-[120px]" />
  </div>
</template>
