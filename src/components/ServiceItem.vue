<script setup lang="ts">
import Button from './ui/button/Button.vue'

interface Props {
  imageSrc: string
  imageAlt: string
  buttonText: string
}

defineProps<Props>()
</script>

<template>
  <div class="grid place-items-center">
    <img :src="imageSrc" :alt="imageAlt" class="h-64 rounded-xl object-cover sm:h-52 lg:h-64" />
    <Button
      class="z-10 -mt-6 w-fit rounded-full px-14 py-6 text-center text-xl font-medium duration-300 ease-in-out hover:bg-button/100 hover:text-black"
    >
      {{ buttonText }}
    </Button>
  </div>
</template>
