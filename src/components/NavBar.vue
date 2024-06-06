<script setup lang="ts">
import { ref } from 'vue'
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

const dialogOpen = ref(false)

const scrollTo = (id: string) => {
  const element = document.getElementById(id)
  if (element) {
    const offset = -50
    const elementPosition = element.getBoundingClientRect().top + window.scrollY
    const offsetPosition = elementPosition + offset
    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    })
  }
  dialogOpen.value = false // Close the dialog after scrolling
}
</script>

<template>
  <div>
    <div
      class="navbar-shadow mx-auto flex h-[80px] max-w-[1080px] items-center justify-between rounded-xl bg-white px-5 py-4 shadow-lg md:h-[88px]"
    >
      <div class="grid place-items-center">
        <img
          @click="scrollTo('header')"
          class="h-[72px] w-auto cursor-pointer duration-100 ease-in hover:scale-105"
          src="../assets/img/logo-horizontal.png"
          alt="Logo-WWEHGER"
        />
      </div>

      <!-- MD AND ABOVE -->
      <ul class="hidden cursor-pointer gap-11 font-medium md:flex">
        <li @click="scrollTo('aboutus')">Über uns</li>
        <li @click="scrollTo('service')">Service</li>
        <li @click="scrollTo('leistungen')">Leistungen</li>
        <li @click="scrollTo('process')">Prozess</li>
      </ul>

      <Button @click="scrollTo('contact')" class="hidden rounded-full bg-button text-black md:flex"
        ><UserRound class="mr-1.5 w-5" />Kontakt</Button
      >

      <!-- MOBILE MENU -->
      <div class="flex md:hidden">
        <Dialog v-model:open="dialogOpen">
          <DialogTrigger as-child>
            <Menu class="cursor-pointer" />
          </DialogTrigger>

          <DialogContent class="max-w-xs rounded-lg md:max-w-md">
            <DialogHeader>
              <DialogTitle>Wir helfen Ihnen gerne!</DialogTitle>
              <DialogDescription>Hier finden Sie uns schnell und einfach.</DialogDescription>
            </DialogHeader>

            <div class="grid gap-2.5">
              <div class="grid gap-2">
                <Button class="rounded-xl" @click="scrollTo('hero')">Home</Button>
                <Button class="rounded-xl" @click="scrollTo('aboutus')">Über Uns</Button>
                <Button class="rounded-xl" @click="scrollTo('service')">Service</Button>
                <Button class="rounded-xl" @click="scrollTo('leistungen')">Leistungen</Button>
              </div>

              <div class="flex gap-2">
                <Button @click="scrollTo('contact')" class="w-full rounded-xl"
                  ><Phone class="mr-1.5 w-5" />Kontakt</Button
                >
                <Button @click="scrollTo('contact')" class="w-full rounded-xl"
                  ><Mail class="mr-1.5 w-5" />Mail</Button
                >
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
