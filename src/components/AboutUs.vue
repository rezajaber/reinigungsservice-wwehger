<script setup lang="ts">
import Button from './ui/button/Button.vue'
import { Stars, BadgeCheck, Phone } from 'lucide-vue-next'

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
    <div class="mx-auto grid max-w-[1280px] justify-between gap-16 lg:flex">
      <div class="grid place-items-center md:place-items-start lg:w-1/2">
        <img
          class="h-56 rounded-xl object-cover sm:h-96 lg:h-full"
          src="../assets/img/about-us.jpeg"
          alt=""
        />
      </div>

      <!-- RIGHT SIDE -->
      <div class="lg:w-1/2">
        <div class="flex gap-1.5">
          <Stars class="w-5 animate-pulse fill-button stroke-button" />
          <h6 class="font-medium tracking-wide text-header">ÜBER UNS</h6>
        </div>

        <h3 class="mt-2 text-5xl sm:text-6xl">Wir sind für Sie da!<br />Bereit & engagiert</h3>
        <p class="mt-7 text-lg opacity-80">
          Unser junges und engagiertes Team sorgt dafür, dass Ihr Auftrag stets nach Ihren Wünschen
          erfolgt und wir mit unserem umfassenden Service Ihre Zufriedenheit sicherstellen.
        </p>

        <ul class="mt-4 grid gap-2">
          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="w-6 fill-header stroke-[#f0f4fa]" />
            Professioneller Service, auf den Sie sich verlassen können.
          </li>

          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="w-6 fill-header stroke-[#f0f4fa]" />
            Ausführung unserer Dienstleistungen mit höchster Präzision.
          </li>

          <li class="flex items-center gap-2 text-lg opacity-90">
            <BadgeCheck class="w-6 fill-header stroke-[#f0f4fa]" />
            Zufriedenheit garantiert durch unsere Expertise und Erfahrung.
          </li>
        </ul>

        <div class="mt-8 grid items-center gap-4 sm:flex">
          <Button
            @click="scrollTo('leistungen')"
            class="h-14 rounded-full bg-button px-12 text-black hover:bg-button/80"
            >Unsere Leistungen</Button
          >

          <div class="flex items-center gap-4">
            <Phone
              class="h-autp h-14 w-14 cursor-pointer rounded-full border-2 border-button fill-header stroke-none p-3.5 duration-300 ease-in-out hover:bg-button hover:fill-black"
            />

            <a href="tel:+49 178 1797307">
              <div class="grid">
                <span class="text-lg opacity-60">Unser Kontakt</span>
                <span class="text-xl font-medium">+49 178 1797307</span>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
