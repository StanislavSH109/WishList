<template>
  <app-card v-for="(item, index) in cards"
   :card="item" :index="index"
   :key="item.id"
   @click="$event => emit('click-by-card', item)"
  />
</template>

<script setup>
import AppCard from './AppCard.vue'

const props = defineProps({
  cards: {
    type: Array,
  },
})
</script>

<style scoped></style>
