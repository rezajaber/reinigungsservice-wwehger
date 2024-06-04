<script setup lang="ts">
import Button from './ui/button/Button.vue'
import { Stars, ArrowRight } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto max-w-[1280px]">
      <!-- TITLE -->
      <div class="needed-for-2/3/2">
        <div>
          <div class="flex gap-1.5">
            <Stars class="w-5 animate-pulse fill-button stroke-button" />
            <h6 class="font-medium tracking-wide text-header">LEISTUNGEN</h6>
          </div>

          <div class="grid gap-5 md:flex md:gap-14">
            <h2 class="mt-2.5 text-6xl font-medium text-white">
              Elevate Your Space with Our Service
            </h2>

            <div>
              <p class="mb-4 text-xl text-sub">
                Exteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
                mollit anim id est laborum.
              </p>

              <div class="flex cursor-pointer items-center gap-1.5">
                <p variant="ghost" class="talk-underline px-0 text-lg text-white">Let's talk</p>
                <ArrowRight class="ml-1.5 w-5 stroke-white" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- GRID -->
      <div class="mt-14 flex flex-wrap justify-center gap-6">
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-one.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Winterdienst</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-two.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Wohnungsauflösung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-three.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Entrümplung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-four.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Hausmeisterservice</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-five.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Gartenarbeiten</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-six.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Entsorgung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-64 rounded-xl object-cover sm:h-52 lg:h-64"
            src="../assets/img/services/service-six.jpg"
            alt=""
          />
          <Button
            class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium hover:bg-header"
            >Reinigung</Button
          >
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.talk-underline {
  position: relative; /* Needed to position the ::after element */
  transition: transform 0.3s ease-in-out;
}

.talk-underline::after {
  content: '';
  position: absolute;
  bottom: -2px; /* Adjust according to the desired distance from the text */
  left: 0;
  width: 0;
  height: 2px; /* Adjust according to the desired thickness of the underline */
  background-color: currentColor; /* Use the text color */
  transition: width 0.3s ease-in-out;
}

.talk-underline:hover::after {
  width: 100%;
}

.talk-underline:hover {
  transform: scale(1.05);
}

/* Hover effect for the droplets icon */
.group:hover .droplets-icon {
  background-color: green !important;
  stroke: white;
}
</style>
