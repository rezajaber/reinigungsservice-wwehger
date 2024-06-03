<script setup lang="ts">
import Button from './ui/button/Button.vue'
import { Stars, BadgeCheck, Phone } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto grid max-w-[1080px] justify-between gap-16 lg:flex">
      <div class="lg:w-1/2">
        <img class="h-full rounded-xl object-cover" src="../assets/img/about-card-3.jpeg" alt="" />
      </div>

      <!-- RIGHT SIDE -->
      <div class="lg:w-1/2">
        <div class="flex gap-1.5">
          <Stars class="fill-button stroke-button w-5 animate-pulse" />
          <h6 class="text-header font-medium tracking-wide">ABOUT US</h6>
        </div>

        <h3 class="mt-2 text-5xl sm:text-6xl">We Make Places <br />Clean & Bright</h3>
        <p class="mt-7 text-lg opacity-80">
          Duis aute irure dolor in repreh ation ullamco laboris nisi ut aliquip onsequa ptate veli
          giat nulla pariatur.
        </p>

        <ul class="mt-4 grid gap-2">
          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="fill-header w-6 stroke-[#f0f4fa]" />
            Ullamco laboris nisi ut aliquip ex ea commodo consequat.
          </li>

          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="fill-header w-6 stroke-[#f0f4fa]" />
            Duis aute irure dolor in reprehenderit in voluptate
          </li>

          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="fill-header w-6 stroke-[#f0f4fa]" />
            Excepteur sint occaecat cupidatat non proiden ulpa qui
          </li>
        </ul>

        <div class="mt-8 flex items-center gap-4">
          <Button class="bg-button hover:bg-button/80 h-14 rounded-full px-12 text-black"
            >Our Services</Button
          >

          <div class="flex items-center gap-4">
            <Phone
              class="fill-header border-button h-autp hover:bg-button h-14 w-14 cursor-pointer rounded-full border stroke-none p-3.5 duration-300 ease-in-out hover:fill-black"
            />
            <div class="grid">
              <span class="text-lg opacity-60">Call Us</span>
              <span class="text-xl font-medium">+123-456-7890</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
