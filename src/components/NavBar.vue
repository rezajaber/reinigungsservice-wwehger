<script setup lang="ts">
import Button from './ui/button/Button.vue'
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogHeader,
  DialogTitle,
  DialogTrigger
} from '@/components/ui/dialog'

import { UserRound, Menu, Mail, Phone } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div
      class="navbar-shadow mx-auto flex h-[80px] max-w-[1080px] items-center justify-between rounded-xl bg-white px-5 py-4 shadow-lg md:h-[88px]"
    >
      <img class="h-8 w-auto md:h-10" src="../assets/img/logo.png" alt="Logo-WWEHGER" />

      <!-- MD AND ABOVE -->
      <ul class="hidden cursor-pointer gap-11 font-medium md:flex">
        <li>Home</li>
        <li>Vorteile</li>
        <li>Über Uns</li>
        <li>Leistungen</li>
      </ul>

      <Button class="hidden rounded-full bg-button text-black md:flex"
        ><UserRound class="mr-1.5 w-5" />Kontakt</Button
      >

      <!-- MOBILE MENU -->
      <div class="flex md:hidden">
        <Dialog>
          <DialogTrigger as-child>
            <Menu class="cursor-pointer" />
          </DialogTrigger>

          <DialogContent class="max-w-xs rounded-lg md:max-w-md">
            <DialogHeader>
              <DialogTitle>Wir helfen Ihnen gerne!</DialogTitle>
              <DialogDescription> Hier finden sie uns schnell und einfach. </DialogDescription>
            </DialogHeader>

            <div class="grid gap-2.5">
              <div class="grid gap-2">
                <Button class="rounded-xl">Home</Button>
                <Button class="rounded-xl">Vorteile</Button>
                <Button class="rounded-xl">Über Uns</Button>
                <Button class="rounded-xl">Leistungen</Button>
              </div>

              <div class="flex gap-2">
                <Button class="w-full rounded-xl"><Mail class="mr-1.5 w-5" />Kontakt</Button>
                <Button class="w-full rounded-xl"><Phone class="mr-1.5 w-5" />Mail</Button>
              </div>
            </div>
          </DialogContent>
        </Dialog>
      </div>
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
  bottom: -31px; /* Adjust according to the desired distance from the text */
  left: 0;
  width: 0;
  height: 3px; /* Adjust according to the desired thickness of the underline */
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
