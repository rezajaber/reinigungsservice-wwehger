<script setup lang="ts">
import Button from './ui/button/Button.vue'

interface Props {
  imageSrc: string
  imageAlt: string
  buttonText: string
  descriptionText: string
}

defineProps<Props>()

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
  <div
    @click="scrollTo('contact')"
    class="group relative grid cursor-pointer place-content-center place-items-center duration-300 ease-in-out hover:scale-[1.03]"
  >
    <img
      :src="imageSrc"
      :alt="imageAlt"
      class="h-64 rounded-xl object-cover duration-300 ease-in-out group-hover:brightness-50"
    />
    <p
      class="absolute inset-0 flex items-center justify-center opacity-0 duration-300 ease-in-out group-hover:opacity-100"
    >
      <span class="-mt-6 rounded-lg bg-opacity-70 px-4 text-center text-xs font-medium text-white">
        {{ descriptionText }}
      </span>
    </p>
    <Button
      class="text-md z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center font-medium duration-300 ease-in-out group-hover:bg-button/100 group-hover:text-black"
    >
      {{ buttonText }}
    </Button>
  </div>
</template>

<style scoped>
/* Additional styles can go here if needed */
</style>
