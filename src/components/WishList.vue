<template>
    <app-card v-for="item in cards" :card="item" :index="index" :key="item.id" />
</template>

<script setup>
import { ref } from 'vue'
import AppCard from './AppCard.vue'

const cards = ref([
  {
    id: 1,
    title: 'Ноутбук',
    description: 'Хочу получить ноутбук к новому году',
    isDone: true,
  },
  {
    id: 2,
    title: 'Мышка',
    description: 'Хочу получить мышку к новому году',
    isDone: false,
  },
  {
    id: 3,
    title: 'Клавиатуру',
    description: 'Хочу получить клавиаутуру к новому году',
    isDone: false,
  },
  {
    id: 4,
    title: 'Колонки',
    description: 'Хочу получить крутые колонки к новому году',
    isDone: true,
  },
  {
    id: 5,
    title: 'Монитор',
    description: 'Хочу получить монитор Samsung к новому году',
    isDone: false,
  },
  {
    id: 6,
    title: 'Вещи для бега',
    description: 'Хочу получить вещи для бега на улице к новому году',
    isDone: true,
  },
])
</script>

<style scoped>

</style>
