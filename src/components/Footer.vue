<script setup lang="ts">
import Credentials from './Credentials.vue'

import { ref } from 'vue'
import { Phone, Facebook, Twitter, Instagram, Linkedin } from 'lucide-vue-next'

const currentYear = ref(new Date().getFullYear())

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
}
</script>

<template>
  <div>
    <div class="container mx-auto max-w-[1280px] p-6">
      <div
        class="background-picture grid place-content-center place-items-center gap-4 rounded-xl px-20 py-10 lg:flex lg:justify-between lg:py-16"
      >
        <div class="text-center lg:text-start">
          <h3 class="mb-3 text-4xl font-medium text-white lg:text-5xl">Kontaktieren Sie Uns</h3>
          <span class="text-lg text-white lg:text-xl"
            >Rufen Sie uns an und bekommen ein kostenloses Angebot!</span
          >
        </div>
        <div class="right-0 mt-4 grid place-items-center gap-4 lg:flex lg:items-center">
          <Phone
            class="h-16 w-16 cursor-pointer rounded-full border-2 border-button bg-button fill-black stroke-none p-3.5 duration-300 ease-in-out"
          />
          <a href="tel:+49 178 1797307">
            <div class="grid">
              <span class="text-center text-xl text-white opacity-80 lg:text-start"
                >Unser Kontakt</span
              >
              <span
                class="text-center text-sm font-medium text-white sm:text-xl lg:text-2xl 2xl:text-4xl"
                >+49 178 1797307</span
              >
            </div>
          </a>
        </div>
      </div>

      <div class="mt-20 lg:flex">
        <div class="-mx-6 w-full lg:w-2/5">
          <div class="px-6">
            <span @click="scrollTo('header')" class="cursor-pointer">
              <img
                class="h-10 w-auto invert duration-100 ease-in hover:scale-105"
                src="../assets/img/logo.png"
                alt=""
              />
            </span>

            <p class="mt-4 max-w-sm text-sub">
              Willkommen bei WWEHGER, hier finden Sie <br />"PERFEKTION IN JEDER DIENSTLEISTUNG"
            </p>

            <div class="mt-4 flex items-center gap-5">
              <a href="https://www.instagram.com/wwehger/">
                <Instagram class="w-6 fill-white duration-300 hover:scale-105 hover:fill-button" />
              </a>
              <a href="">
                <Facebook
                  class="w-5 fill-white stroke-white duration-300 hover:scale-105 hover:fill-button hover:stroke-button"
                />
              </a>
              <a href="">
                <Linkedin
                  class="w-5 fill-white stroke-white duration-300 hover:scale-105 hover:fill-button hover:stroke-button"
                />
              </a>
              <a href="">
                <Twitter
                  class="w-5 fill-white stroke-white duration-300 hover:scale-105 hover:fill-button hover:stroke-button"
                />
              </a>
            </div>
          </div>
        </div>

        <div class="mt-6 lg:mt-0 lg:flex-1">
          <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
            <div>
              <h3
                @click="scrollTo('service')"
                class="cursor-pointer uppercase text-white hover:underline"
              >
                Service
              </h3>
              <span
                @click="scrollTo('service')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Qualitätsservice</span
              >
              <span
                @click="scrollTo('service')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Professionalität</span
              >
              <span
                @click="scrollTo('service')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Preisgestaltung</span
              >
              <span
                @click="scrollTo('service')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Zufriedenheit</span
              >
            </div>

            <div>
              <h3
                @click="scrollTo('leistungen')"
                class="cursor-pointer uppercase text-white hover:underline"
              >
                Leistungen
              </h3>
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Winterdienst</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Wohnungsauflösung</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Entrümplung</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Entrümplung</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Hausmeisterservice</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Gartenarbeiten</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Entsorgung</span
              >
              <span
                @click="scrollTo('leistungen')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Reinigung</span
              >
            </div>

            <div>
              <h3
                @click="scrollTo('process')"
                class="cursor-pointer uppercase text-white hover:underline"
              >
                Prozess
              </h3>
              <span
                @click="scrollTo('process')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Service wählen</span
              >
              <span
                @click="scrollTo('process')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Team kommt</span
              >
              <span
                @click="scrollTo('process')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Prozessstart</span
              >
              <span
                @click="scrollTo('process')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Zufriedenheit</span
              >
            </div>

            <div>
              <h3
                @click="scrollTo('aboutus')"
                class="cursor-pointer uppercase text-white hover:underline"
              >
                Über uns
              </h3>
              <span
                @click="scrollTo('aboutus')"
                class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                >Sektion</span
              >
              <span class="mt-2 block cursor-pointer text-sm text-sub hover:underline"
                ><Credentials
              /></span>
            </div>
          </div>
        </div>
      </div>

      <hr class="my-6 h-px border-none bg-gray-200" />

      <div>
        <p class="text-center text-sub">© WWEHGER {{ currentYear }} - All rights reserved</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.background-picture {
  background-image: url('../assets/img/contact-us.png');
  /* You might want to adjust these properties based on your image and layout */
  background-size: cover;
  background-position: center;
}
</style>
