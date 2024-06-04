<script setup lang="ts">
import Header from '../components/Header.vue'
import NavBar from '../components/NavBar.vue'
import Hero from '../components/Hero.vue'
import Vorteile from '../components/Vorteile.vue'
import AboutUs from '../components/AboutUs.vue'
import Service from '../components/Service.vue'
import Process from '../components/Process.vue'

import Footer from '../components/Footer.vue'

import darkWallImage from '../assets/img/dark-wall.png'
import WallImage from '../assets/img/wall.jpeg'
</script>

<template>
  <div>
    <Header id="header" class="h-[88px] bg-header px-5 2xl:px-0" />
    <NavBar class="fixed inset-x-0 z-50 -mt-[45px] px-5 2xl:px-0" />
    <div id="hero">
      <Hero />
    </div>
    <div id="service">
      <Vorteile class="px-5 py-[120px] 2xl:px-0" />
    </div>
    <div id="aboutus">
      <AboutUs class="bg-[#f0f4fa] px-5 py-[120px] 2xl:px-0" />
    </div>
    <div id="leistungen">
      <Service
        :style="{ backgroundImage: `url(${darkWallImage})` }"
        class="bg-cover bg-center px-5 py-[120px] 2xl:px-0"
      />
    </div>
    <div id="process">
      <Process
        :style="{ backgroundImage: `url(${WallImage})` }"
        class="bg-cover bg-center px-5 py-[120px] 2xl:px-0"
      />
    </div>
    <Footer id="contact" class="bg-[#0F2E38] px-5 py-[60px] 2xl:px-0" />
  </div>
</template>
