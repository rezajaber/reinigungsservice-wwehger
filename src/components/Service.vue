<script setup lang="ts">
import { Stars, ArrowRight } from 'lucide-vue-next'
import ServiceItem from './ServiceItem.vue'

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

const services = [
  {
    src: './src/assets/img/services/service-one.jpg',
    alt: 'Wohnungsauflösung',
    text: 'Wohnungsauflösung'
  },

  {
    src: './src/assets/img/services/service-two.jpg',
    alt: 'Entrümplung / Entsorgung',
    text: 'Entrümplung / Entsorgung'
  },
  {
    src: './src/assets/img/services/service-three.jpg',
    alt: 'Abrissarbeiten',
    text: 'Abrissarbeiten'
  },
  {
    src: './src/assets/img/services/service-four.jpg',
    alt: 'Hausmeisterservice',
    text: 'Hausmeisterservice'
  },
  {
    src: './src/assets/img/services/service-five.jpg',
    alt: 'Gartenarbeiten',
    text: 'Gartenarbeiten'
  },
  { src: './src/assets/img/services/service-six.jpg', alt: 'Winterdienst', text: 'Winterdienst' },
  {
    src: './src/assets/img/services/service-one.jpg',
    alt: 'Gebäudereinigung',
    text: 'Gebäudereinigung'
  }
]
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
            <h2 class="mt-2.5 text-5xl font-medium text-white md:text-6xl">
              Verwandeln Sie Ihren Raum
            </h2>
            <div>
              <p class="mb-4 text-xl text-sub">
                Wir machen Ihr Zuhause und oder Ihren Arbeitsplatz zu einem sauberen und
                wohlfühlendem Ort zu machen.
              </p>
              <div class="flex cursor-pointer items-center gap-1.5">
                <p class="talk-underline px-0 text-lg text-white" @click="scrollTo('contact')">
                  Fangen wir an
                </p>
                <ArrowRight class="ml-1.5 w-5 stroke-white" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- GRID -->
      <div class="mt-14 flex flex-wrap justify-center gap-6">
        <ServiceItem
          v-for="service in services"
          :key="service.text"
          :imageSrc="service.src"
          :imageAlt="service.alt"
          :buttonText="service.text"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.talk-underline {
  position: relative;
  transition: transform 0.3s ease-in-out;
}

.talk-underline::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: currentColor;
  transition: width 0.3s ease-in-out;
}

.talk-underline:hover::after {
  width: 100%;
}

.talk-underline:hover {
  transform: scale(1.05);
}

.group:hover .droplets-icon {
  background-color: green !important;
  stroke: white;
}
</style>
