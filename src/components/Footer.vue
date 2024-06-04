<script setup lang="ts">
import { Phone, Facebook, Twitter, Instagram, Linkedin } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="container mx-auto max-w-[1280px] p-6">
      <div
        class="grid place-items-center gap-4 rounded-xl bg-header px-20 py-10 lg:flex lg:justify-between lg:py-16"
      >
        <div class="text-center lg:text-start">
          <h3 class="mb-3 text-4xl font-medium text-white lg:text-5xl">Call for A Free Quote</h3>
          <span class="text-lg text-white lg:text-xl"
            >Exteur sint occaecat cupidatat non proident</span
          >
        </div>

        <div class="right-0 mt-4 flex items-center gap-4">
          <Phone
            class="h-16 w-16 cursor-pointer rounded-full border-2 border-button bg-button fill-black stroke-none p-3.5 duration-300 ease-in-out"
          />
          <div class="grid">
            <span class="text-xl text-white opacity-80">Call Us Now</span>
            <span class="text-xl font-medium text-white lg:text-2xl 2xl:text-4xl"
              >+123-456-7890</span
            >
          </div>
        </div>
      </div>

      <div class="mt-20 lg:flex">
        <div class="-mx-6 w-full lg:w-2/5">
          <div class="px-6">
            <a href="#">
              <img class="h-10 w-auto invert" src="../assets/img/logo.png" alt="" />
            </a>

            <p class="mt-4 max-w-sm text-sub">
              Join 31,000+ other and never miss out on new tips, tutorials, and more.
            </p>

            <div class="mt-4 flex gap-5">
              <Instagram class="w-6 fill-white stroke-[#0F2E38]" />
              <Facebook class="w-5 fill-white stroke-white" />
              <Linkedin class="w-5 fill-white stroke-white" />
              <Twitter class="w-5 fill-white stroke-white" />
            </div>
          </div>
        </div>

        <div class="mt-6 lg:mt-0 lg:flex-1">
          <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
            <div>
              <h3 class="uppercase text-white">About</h3>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Company</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">community</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Careers</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Blog</h3>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Tec</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Music</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Videos</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Products</h3>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Mega cloud</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Aperion UI</a>
              <a href="#" class="mt-2 block text-sm text-sub hover:underline">Meraki UI</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Contact</h3>
              <span class="mt-2 block text-sm text-sub hover:underline">+1 526 654 8965</span>
              <span class="mt-2 block text-sm text-sub hover:underline">example@email.com</span>
            </div>
          </div>
        </div>
      </div>

      <hr class="my-6 h-px border-none bg-gray-200" />

      <div>
        <p class="text-center text-sub">© WWEHGER 2024 - All rights reserved</p>
      </div>
    </div>
  </div>
</template>
