<script setup lang="ts">
import Button from './ui/button/Button.vue'
import {
  Sheet,
  SheetContent,
  SheetDescription,
  SheetHeader,
  SheetTitle,
  SheetTrigger
} from '@/components/ui/sheet'

import { Phone, Mail } from 'lucide-vue-next'
</script>

<template>
  <Sheet>
    <div class="grid place-items-start gap-2">
      <SheetTrigger class="px-0 hover:underline">Impressum </SheetTrigger>
      <SheetTrigger class="px-0 hover:underline">Datenschutz </SheetTrigger>
    </div>

    <SheetContent>
      <SheetHeader>
        <div class="grid gap-8">
          <div class="grid gap-2">
            <SheetTitle class="text-2xl font-medium">Impressum</SheetTitle>
            <SheetDescription>
              <div class="flex flex-wrap gap-2">
                <Button class="hover:bg-header/100"> Bljerim Zaiti</Button>
                <Button class="hover:bg-header/100">Walddörferstraße 1A</Button>
                <Button class="hover:bg-header/100"> 22041 Hamburg</Button>
                <Button class="hover:bg-header/100"
                  ><Phone class="mr-1.5 w-5" /> +49 178 1797307</Button
                >
                <Button class="hover:bg-header/100"
                  ><Mail class="mr-1.5 w-5" />bljerim.zaiti@web.de</Button
                >
              </div>
            </SheetDescription>
          </div>
          <div class="grid gap-2">
            <SheetTitle class="text-2xl font-medium">Datenschutz </SheetTitle>
            <SheetDescription>
              <div class="flex flex-wrap gap-2 text-justify">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo accusantium sequi
                alias dolorum, debitis inventore, iusto neque tempora perferendis labore quas esse
                assumenda ex, dolores dicta voluptatum pariatur! Animi, consectetur. Lorem ipsum
                dolor sit amet consectetur, adipisicing elit. Repudiandae ab eius rem maxime, veniam
                cupiditate itaque atque cumque iste quisquam, distinctio fugit temporibus
                dignissimos praesentium optio eveniet accusamus dolores nobis. Lorem, ipsum dolor
                sit amet consectetur adipisicing elit. Dicta perferendis ipsum cumque odit nemo,
                ullam eos dolorum voluptatibus consectetur? Voluptatum pariatur ipsa sed quia dicta
                eos aut in fugit molestiae. Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Optio repudiandae dolor nostrum, ea amet quibusdam accusamus placeat eveniet
                voluptates nihil, nemo natus est ad nobis repellendus distinctio perferendis dicta!
                Dolor. Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat tempore
                necessitatibus corporis eos libero qui deleniti reprehenderit alias, quas ipsa natus
                voluptatem odio sit suscipit consequuntur sapiente. Quam, dignissimos assumenda.
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi veniam suscipit
                corporis assumenda laboriosam tempore, delectus necessitatibus magnam odio harum
                autem et iusto laudantium deserunt, placeat incidunt laborum minus sequi. Lorem
                ipsum dolor sit amet consectetur adipisicing elit. Numquam consequuntur totam hic
                mollitia labore, iste possimus, doloribus assumenda exercitationem unde iure
                similique quod aut animi accusamus necessitatibus veritatis vitae! Aut. Lorem, ipsum
                dolor sit amet consectetur adipisicing elit. Eaque, dolor necessitatibus iste
                delectus deleniti provident natus ducimus suscipit quo. Voluptatibus suscipit amet
                natus esse eos enim culpa explicabo illum fuga. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Nobis accusantium autem quia. Iste aliquid similique
                rem obcaecati delectus maiores ex inventore ea quasi modi? A dolores ratione iusto
                in deleniti. Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil
                recusandae non aspernatur minus eius laborum totam aut magni perspiciatis quidem
                fuga sed, ratione nam porro praesentium temporibus dolorem doloremque asperiores.
              </div>
            </SheetDescription>
          </div>
        </div>
      </SheetHeader>
    </SheetContent>
  </Sheet>
</template>
