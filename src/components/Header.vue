<script setup lang="ts">
import { Phone, Mail, MapPin, Facebook, Twitter, Instagram, Linkedin } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto flex max-w-[1080px] items-start justify-between">
      <!-- HEADER TABLET & ABOVE -->
      <div class="mt-2.5 flex items-center gap-5">
        <a href="tel:+49 178 1797307">
          <div class="flex items-center gap-2 text-white duration-300 hover:scale-105">
            <Phone class="w-5 fill-white stroke-none" />
            <span class="hidden text-sm md:block lg:text-base">+49 178 1797307</span>
          </div>
        </a>

        <span class="hidden font-extralight text-white opacity-80 md:block">|</span>
        <a href="mailto:bljerim.zaiti@web.de" target="_blank">
          <div class="flex items-center gap-2 text-white duration-300 hover:scale-105">
            <Mail class="w-5 fill-white stroke-header" />
            <span class="hidden text-sm md:block lg:text-base">bljerim.zaiti@web.de</span>
          </div>
        </a>

        <span class="hidden font-extralight text-white opacity-80 md:block">|</span>

        <a
          href="https://www.google.de/maps/dir//Waldd%C3%B6rferstra%C3%9Fe+1A,+22041+Hamburg/@53.5785076,10.0620684,17z/data=!3m1!4b1!4m8!4m7!1m0!1m5!1m1!1s0x47b189541445cf9b:0xe012f9910fdc0137!2m2!1d10.0646433!2d53.5785076?entry=ttu"
          target="_blank"
        >
          <div class="flex items-center gap-2 text-white duration-300 hover:scale-105">
            <MapPin class="w-5" />
            <span class="hidden text-sm md:block lg:text-base">Walddörferstraße 1A</span>
          </div>
        </a>
      </div>

      <div class="mt-2.5 flex items-center gap-5">
        <a href="https://www.instagram.com/wwehger/" target="_blank">
          <Instagram
            class="w-6 fill-white stroke-header duration-300 hover:scale-105 hover:fill-button"
          />
        </a>
        <a href="">
          <Facebook
            class="w-5 fill-white stroke-white duration-300 hover:scale-105 hover:fill-button hover:stroke-button"
          />
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
