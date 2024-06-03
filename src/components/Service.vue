<script setup lang="ts">
import { Stars, ArrowRight, Droplets } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="mx-auto lg:max-w-[1080px]">
      <!-- TITLE -->
      <div class="flex justify-between">
        <div>
          <div class="flex gap-1.5">
            <Stars class="fill-button stroke-button w-5 animate-pulse" />
            <h6 class="text-header font-medium tracking-wide">LEISTUNGEN</h6>
          </div>

          <div class="flex">
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
      <div class="mt-14 grid grid-cols-3 gap-6">
        <div class="group relative overflow-hidden rounded-xl">
          <img
            class="h-72 w-auto cursor-pointer rounded-xl object-cover"
            src="../assets/img/services/service-one.jpg"
            alt=""
          />

          <div
            class="absolute -bottom-[104px] bg-white px-12 pb-8 pt-4 duration-300 ease-in group-hover:-bottom-0"
          >
            <Droplets
              class="droplets-icon bg-button hover:bg-header absolute -top-8 right-5 h-16 w-16 rounded-full p-3 duration-100 ease-in-out"
            />
            <p class="text-2xl font-medium">Plumbing Service</p>
            <p class="mt-10 opacity-80">
              Duis aute irure dolor in repreh ation ullamco laboris nisi
            </p>
          </div>
        </div>
        <img
          class="h-full rounded-xl object-cover"
          src="../assets/img/services/service-two.jpg"
          alt=""
        />
        <img
          class="h-full rounded-xl object-cover"
          src="../assets/img/services/service-three.jpg"
          alt=""
        />
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
