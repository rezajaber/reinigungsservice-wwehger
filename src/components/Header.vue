<script setup lang="ts">
import { Phone, Mail, MapPin, Facebook, Twitter, Instagram, Linkedin } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto flex max-w-[1080px] items-start justify-between">
      <!-- HEADER TABLET & ABOVE -->
      <div class="mt-2.5 flex items-center gap-4">
        <div class="flex items-center gap-2 text-white">
          <Phone class="w-5 fill-white stroke-none" />
          <span>+123 456 7890</span>
        </div>

        <span class="font-extralight text-white opacity-80">|</span>

        <div class="flex items-center gap-2 text-white">
          <Mail class="stroke-header w-5 fill-white" />
          <span>+123 456 7890</span>
        </div>

        <span class="font-extralight text-white opacity-80">|</span>

        <div class="flex items-center gap-2 text-white">
          <MapPin class="w-5" />
          <span>+123 456 7890</span>
        </div>
      </div>

      <div class="mt-2.5 flex items-center gap-5">
        <Instagram class="stroke-header w-6 fill-white" />
        <Facebook class="w-5 fill-white stroke-white" />
        <Linkedin class="w-5 fill-white stroke-white" />
        <Twitter class="w-5 fill-white stroke-white" />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
