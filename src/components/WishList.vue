<template>
  <div class="container">
    <h1 class="title">Wish List</h1>
    <div class="wrapper">
      <div class="card" v-for="item in cards" :key="item.id">
        <div class="card__title">{{ item.title }}</div>
        <div class="card__description">{{ item.description }}</div>
        <div class="card__is-actived">
          <div :class="{ 'card__is-active': item.isDone, 'card__is-not-active': !item.isDone }">
            {{ item.isDone ? 'Исполнено' : 'Не исполнено' }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

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

<style scoped></style>
