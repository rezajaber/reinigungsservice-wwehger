<script setup lang="ts">
import { Phone, Mail, MapPin, Facebook, Twitter, Instagram, Linkedin } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="container mx-auto p-6">
      <div class="lg:flex">
        <div class="-mx-6 w-full lg:w-2/5">
          <div class="px-6">
            <a href="#">
              <img class="h-10 w-auto invert" src="../assets/img/logo.png" alt="" />
            </a>

            <p class="text-sub mt-4 max-w-sm">
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
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Company</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">community</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Careers</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Blog</h3>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Tec</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Music</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Videos</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Products</h3>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Mega cloud</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Aperion UI</a>
              <a href="#" class="text-sub mt-2 block text-sm hover:underline">Meraki UI</a>
            </div>

            <div>
              <h3 class="uppercase text-white">Contact</h3>
              <span class="text-sub mt-2 block text-sm hover:underline">+1 526 654 8965</span>
              <span class="text-sub mt-2 block text-sm hover:underline">example@email.com</span>
            </div>
          </div>
        </div>
      </div>

      <hr class="my-6 h-px border-none bg-gray-200" />

      <div>
        <p class="text-sub text-center">© WWEHGER 2024 - All rights reserved</p>
      </div>
    </div>
  </div>
</template>
