<script setup lang="ts">
import { Stars, BriefcaseBusiness, Users, BadgeEuro } from 'lucide-vue-next'

const cards = [
  {
    icon: BriefcaseBusiness,
    title: 'Qualitätsservice:',
    description:
      'Unser Service steht für Qualität auf höchstem Niveau. Wir verwenden nur die besten Materialien und modernste Techniken, um sicherzustellen, dass jede Aufgabe perfekt erledigt wird.'
  },
  {
    icon: Users,
    title: 'Professionalität:',
    description:
      'Unser junges, engagiertes und freundliches Team ist hochqualifiziert und erfahren. Jeder Mitarbeiter bringt sein Fachwissen und seine Leidenschaft in die Arbeit ein, um Ihnen den bestmöglichen Service zu bieten.'
  },
  {
    icon: BadgeEuro,
    title: 'Preisgestaltung:',
    description:
      'Wir bieten erstklassigen Service zu erschwinglichen Preisen. Unser Ziel ist es, Ihnen die beste Leistung zu einem fairen Preis zu bieten, damit Sie ohne Kompromisse profitieren können.'
  },
  {
    icon: Stars,
    title: 'Zufriedenheit:',
    description:
      'Unsere Kundenbewertungen sprechen für sich – exzellenter Service, zufriedene Kunden. Wir sind stolz auf das positive Feedback und die Weiterempfehlungen unserer zufriedenen Kunden, welche vor allem unsere kollegiale Art mögen.'
  }
]
</script>

<template>
  <div class="relative mx-auto max-w-[1440px]">
    <!-- Stars placed in the background -->
    <Stars
      class="absolute left-10 top-20 z-[-1] h-auto w-8 animate-bounce fill-button stroke-button opacity-80 md:w-14"
    />

    <div>
      <div class="flex items-center justify-center gap-1.5">
        <Stars class="w-5 animate-pulse fill-button stroke-button" />
        <h6 class="font-medium tracking-wide text-header">PROFESSIONELLER SERVICE</h6>
      </div>

      <h3 class="mt-1 text-center text-5xl sm:text-6xl">Unser Service<br />vor Ort</h3>
    </div>

    <div class="mt-14 flex flex-wrap justify-center gap-8">
      <div
        v-for="(card, index) in cards"
        :key="index"
        class="card card-shadow relative z-10 w-80 rounded-lg px-10 py-16 duration-500 ease-in-out hover:-translate-y-2 hover:scale-105"
      >
        <component :is="card.icon" class="icon h-auto w-14 stroke-header" />
        <p class="mt-7 text-2xl font-medium">{{ card.title }}</p>
        <p class="text-md mt-6 opacity-80">
          {{ card.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  box-shadow:
    rgba(14, 30, 37, 0.15) 0px 2px 4px 0px,
    rgba(14, 30, 37, 0.25) 0px 2px 16px 0px;
}

@keyframes spinX {
  from {
    transform: rotateY(0deg);
  }
  to {
    transform: rotateY(360deg);
  }
}

.card:hover .icon {
  animation: spinX 0.5s ease-in-out;
}
</style>
