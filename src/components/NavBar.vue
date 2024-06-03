<script setup lang="ts">
import Button from './ui/button/Button.vue'

import { UserRound } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div
      class="navbar-shadow mx-auto flex max-w-[1080px] items-center justify-between rounded-xl bg-white px-5 py-4 shadow-lg"
    >
      <img class="h-10 w-auto" src="../assets/img/logo.png" alt="Logo-WWEHGER" />

      <ul class="flex cursor-pointer gap-11 font-medium">
        <li>Home</li>
        <li>Vorteile</li>
        <li>Über Uns</li>
        <li>Leistungen</li>
      </ul>

      <Button><UserRound class="mr-1.5 w-5" />Kontakt</Button>
    </div>
  </div>
</template>

<style scoped>
.navbar-shadow {
  box-shadow:
    rgba(14, 30, 37, 0.15) 0px 2px 4px 0px,
    rgba(14, 30, 37, 0.25) 0px 2px 16px 0px;
}

li {
  position: relative; /* Needed to position the ::after element */
  transition: transform 0.3s ease-in-out;
}

li::after {
  content: '';
  position: absolute;
  bottom: -23px; /* Adjust according to the desired distance from the text */
  left: 0;
  width: 0;
  height: 2px; /* Adjust according to the desired thickness of the underline */
  background-color: #2bba80; /* Use the text color */
  transition: width 0.3s ease-in-out;
}

li:hover::after {
  width: 100%;
}

li:hover {
  transform: scale(1.05);
}
</style>
