<script setup lang="ts">
import Button from './ui/button/Button.vue'
import { Stars, ArrowRight } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto max-w-[1440px]">
      <!-- TITLE -->
      <div class="needed-for-2/3/2">
        <div>
          <div class="flex gap-1.5">
            <Stars class="fill-button stroke-button w-5 animate-pulse" />
            <h6 class="text-header font-medium tracking-wide">LEISTUNGEN</h6>
          </div>

          <div class="grid gap-5 md:flex md:gap-14">
            <h2 class="mt-2.5 text-6xl font-medium text-white">
              Elevate Your Space with Our Service
            </h2>

            <div>
              <p class="text-sub mb-4 text-xl">
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
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-one.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Winterdienst</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-two.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Wohnungsauflösung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-three.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Entrümplung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-four.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Hausmeisterservice</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-five.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Gartenarbeiten</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-six.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
            >Entsorgung</Button
          >
        </div>
        <div class="grid place-items-center">
          <img
            class="h-72 rounded-xl object-cover"
            src="../assets/img/services/service-six.jpg"
            alt=""
          />
          <Button
            class="hover:bg-header z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium"
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
