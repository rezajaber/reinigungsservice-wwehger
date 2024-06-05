<script setup lang="ts">
import { Stars } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div>
      <div class="flex items-center justify-center gap-1.5">
        <Stars class="w-5 animate-pulse fill-button stroke-button" />
        <h6 class="font-medium tracking-wide text-header">PROZESS</h6>
      </div>

      <h3 class="mt-1 text-center text-5xl sm:text-6xl">So funktioniert's</h3>
    </div>

    <div class="mt-16 flex flex-wrap items-start justify-center gap-20 xl:gap-20 2xl:gap-32">
      <div class="group relative grid place-items-center gap-6">
        <span
          class="absolute left-14 top-0 flex h-11 w-11 items-center justify-center rounded-full bg-button font-semibold transition duration-500 ease-in-out group-hover:bg-green-500 group-hover:text-white"
          >1
        </span>
        <img
          class="h-48 w-48 rounded-full object-cover"
          src="../assets/img/process/process-one.jpeg"
          alt=""
        />
        <p class="text-2xl font-medium">Wählen Sie einen Service</p>
        <p class="w-60 text-center text-[#5E6F92]">
          Wählen Sie aus unserer Liste von Dienstleistungen den passenden für Ihre Bedürfnisse aus.
        </p>
      </div>

      <div class="group relative grid place-items-center gap-6">
        <span
          class="absolute left-7 top-0 flex h-11 w-11 items-center justify-center rounded-full bg-button font-semibold transition duration-500 ease-in-out group-hover:bg-green-500 group-hover:text-white"
          >2
        </span>
        <img
          class="h-48 w-48 rounded-full object-cover"
          src="../assets/img/process/process-two.jpeg"
          alt=""
        />
        <p class="text-2xl font-medium">Team kommt an</p>
        <p class="w-60 text-center text-[#5E6F92]">
          Unser Team trifft pünktlich bei Ihnen ein und beginnt mit den vereinbarten Arbeiten.
        </p>
      </div>

      <div class="group relative grid place-items-center gap-6">
        <span
          class="absolute left-7 top-0 flex h-11 w-11 items-center justify-center rounded-full bg-button font-semibold transition duration-500 ease-in-out group-hover:bg-green-500 group-hover:text-white"
          >3
        </span>
        <img
          class="h-48 w-48 rounded-full object-cover"
          src="../assets/img/process/process-three.jpeg"
          alt=""
        />
        <p class="text-2xl font-medium">Reinigungsprozess</p>
        <p class="w-60 text-center text-[#5E6F92]">
          Wir führen die Reinigung nach höchsten Standards durch, um beste Ergebnisse zu erzielen.
        </p>
      </div>

      <div class="group relative grid place-items-center gap-6">
        <span
          class="absolute left-7 top-0 flex h-11 w-11 items-center justify-center rounded-full bg-button font-semibold transition duration-500 ease-in-out group-hover:bg-green-500 group-hover:text-white"
          >4
        </span>
        <img
          class="h-48 w-48 rounded-full object-cover"
          src="../assets/img/process/process-four.jpeg"
          alt=""
        />
        <p class="text-2xl font-medium">Zufriedenheit</p>
        <p class="w-60 text-center text-[#5E6F92]">
          Ihre Zufriedenheit ist unser oberstes Ziel. Wir stellen sicher, dass Sie mit unserer
          Arbeit vollkommen zufrieden sind.
        </p>
      </div>
    </div>
  </div>
</template>

<style>
@keyframes spinX {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(360deg);
  }
}

.group:hover .bg-button {
  animation: spinX 0.5s linear;
}
</style>
