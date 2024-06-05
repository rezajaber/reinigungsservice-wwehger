<script setup lang="ts"></script>

<template>
  <div class="relative">
    <img
      class="h-[500px] w-full transform object-cover transition-transform duration-500 ease-in-out hover:scale-105 md:h-auto lg:h-[700px] 2xl:h-[800px]"
      src="../assets/img/hero.jpeg"
      alt="Hero Image"
    />
    <div class="absolute inset-0 bg-sky-400 opacity-30"></div>
    <div class="absolute inset-0 bg-black opacity-35"></div>

    <div class="absolute inset-0 flex items-center justify-center p-4 text-center text-white">
      <div class="grid md:gap-5">
        <h3 class="mb-2 font-semibold sm:text-lg md:text-xl">IHR ZUHAUSE, IHR PARADIES</h3>
        <h1 class="mb-4 text-4xl font-semibold sm:text-6xl xl:text-7xl">
          PERFEKTION IN <br />JEDER DIENSTLEISTUNG
        </h1>
        <h6 class="sm:text-md text-sm md:text-lg">
          Wir sind im Dienst – mit Hingabe und Sorgfalt. Unser Team sorgt für Sauberkeit und
          Zufriedenheit.
          <br class="hidden lg:block" />Vertrauen Sie auf unsere Expertise und Leidenschaft.
        </h6>
      </div>
    </div>
  </div>
</template>
