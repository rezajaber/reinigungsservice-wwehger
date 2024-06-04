<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <Transition>
    <RouterView />
  </Transition>
</template>

<style scoped>
/* we will explain what these classes do next! */
.v-enter-active,
.v-leave-active {
  transition: opacity 1s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
