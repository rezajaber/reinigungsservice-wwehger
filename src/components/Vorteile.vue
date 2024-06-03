<script setup lang="ts">
import { Stars, BriefcaseBusiness, Users, BadgeEuro } from 'lucide-vue-next'
</script>

<template>
  <div class="mx-auto max-w-[1440px]">
    <div class="">
      <div class="flex items-center justify-center gap-1.5">
        <Stars class="fill-button stroke-button w-5 animate-pulse" />
        <h6 class="text-header font-medium tracking-wide">PROFESSIONAL SERVICE</h6>
      </div>

      <h3 class="mt-1 text-center text-5xl sm:text-6xl">Cleaning Service at <br />Your Door</h3>
    </div>

    <div class="mt-14 flex flex-wrap justify-center gap-8">
      <div
        v-for="i in 4"
        :key="i"
        class="card-shadow w-80 rounded-lg px-10 py-16 duration-500 ease-in-out hover:-translate-y-2 hover:scale-105"
      >
        <BriefcaseBusiness class="stroke-header h-auto w-14" />
        <p class="mt-7 text-2xl font-medium">Quality Service</p>
        <p class="mt-6 text-lg opacity-80">
          Kobita amco laboris nisid ut aliquip ex ea com moido consequat. Duis aute irure dolor in
          reprehen
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card-shadow {
  box-shadow:
    rgba(14, 30, 37, 0.15) 0px 2px 4px 0px,
    rgba(14, 30, 37, 0.25) 0px 2px 16px 0px;
}
</style>
