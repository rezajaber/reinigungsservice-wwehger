<script setup lang="ts">
import { Stars, ArrowRight } from 'lucide-vue-next'
import ServiceItem from './ServiceItem.vue'

import serviceOne from '../assets/img/service/service-one.jpeg'
import serviceTwo from '../assets/img/service/service-two.jpeg'
import serviceThree from '../assets/img/service/service-three.jpeg'
import serviceFour from '../assets/img/service/service-four.jpeg'
import serviceFive from '../assets/img/service/service-five.jpeg'
import serviceSix from '../assets/img/service/service-six.jpeg'
import serviceSeven from '../assets/img/service/service-one.jpeg'

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
    src: serviceOne,
    alt: 'Umzug & Transport',
    button: 'Umzug & Transport',
    description:
      'Von der Umzugsplanung über den Möbel- und Kistentransport bis hin zu optionalen Services wie dem Auspacken der Umzugskartons, der Möbelmontage sowie Reinigungs-, Maler- und Renovierungsarbeiten. Wir bieten Ihnen ein umfangreiches, individuell angepasstes Angebot und unterstützen Sie mit unseren Services für Ihren Umzug. Wir verhelfen Ihnen zu einem erfolgreichen, angenehmen und besonders für Sie stressfreien Umzug.'
  },
  {
    src: serviceTwo,
    alt: 'Entrümplung | Haushaltsauflösung',
    button: 'Entrümplung | Haushaltsauflösung',
    description:
      'Unser Team steht Ihnen zur Verfügung, wenn Sie ein Unternehmen auflösen, eine Erbschaft erhalten oder Ihren Keller oder Ihre Garage aufräumen müssen. Wir übernehmen die Haushaltsauflösung, schaffen Platz, verwerten nützliche Gegenstände und entsorgen Abfälle jeglicher Art (privat/gewerblich) unter Berücksichtigung der Umweltstandards.'
  },
  {
    src: serviceThree,
    alt: 'Abriss- & Abbrucharbeiten',
    button: 'Abriss- & Abbrucharbeiten',
    description:
      'Wir bieten Abriss- oder Abbrucharbeiten für Teile eines Gebäudes/Anbaus im Innen- oder Außenbereich, komplette Innenraum-Neugestaltung, Erstellung einer Öffnung in der Wand, Einsetzen/Entfernen eines Kamins oder Terrassenabbruch in Ihrem Garten. Mit unserer Expertise in diesem Bereich können wir jede Arbeit flexibel, schnell und problemlos für Sie und nach Ihren speziellen Wünschen erledigen.'
  },
  {
    src: serviceFour,
    alt: 'Hausmeisterservice',
    button: 'Hausmeisterservice',
    description:
      'Sie suchen einen flexiblen und engagierten Hausmeister Ihres Vertrauens für Ihre Immobilie oder Ihr Unternehmen? Oder Sie brauchen nur für einen kleinen Auftrag oder für eine bestimmte kurze Zeit die Dienste eines Hausmeisters? Bei WWEHGER stehen wir mit unseren spezialisierten Hausmeisterdiensten zur Verfügung und freuen uns auf Ihre Anfrage!'
  },
  {
    src: serviceFive,
    alt: 'Gartenarbeiten',
    button: 'Gartenarbeiten',
    description:
      'Sie haben ein kleines Projekt im Garten vor und benötigen jemanden, der Ihre Vision versteht und umsetzen kann, oder wollen zuverlässige Helfer für Rasenmähen, Hecke schneiden, Unkraut zupfen und Co.? Sie besitzen oder managen eine Immobilie oder ein Unternehmen und auch dort soll es in Ihrem Vorgarten gepflegt und ordentlich aussehen? Unser Team ist für Sie und Ihre Wünsche da! Vereinbaren Sie ein Beratungsgespräch oder erfragen Sie ein unverbindliches Angebot.'
  },
  {
    src: serviceSix,
    alt: 'Winterdienst',
    button: 'Winterdienst',
    description:
      'Der zuverlässige Winterdienst für Sie als Privatperson im Vorgarten, für Ihr Büro/Gebäude, ganze Straßen oder sogar mehrere Bezirke und Routen - und das, wenn gewünscht, jederzeit im 24/7-Notfall-Winterdienst!'
  },
  {
    src: serviceSeven,
    alt: 'Reinigungsarbeiten',
    button: 'Reinigungsarbeiten',
    description:
      'Gebäudereinigung für Einzel- oder Großraumbüros, Bürokomplexe, Industriegebäude oder einfache Mehrfamilienhäuser - wir von WWEHGER stehen mit unserem professionellen Team für hygienische Sauberkeit bereit und krempeln die Ärmel hoch.'
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
          :key="service.alt"
          :imageSrc="service.src"
          :imageAlt="service.alt"
          :buttonText="service.button"
          :descriptionText="service.description"
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
