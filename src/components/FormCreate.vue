<template>
  <h2 class="title-form">Форма заполнения {{ newCard.title }}</h2>
  <div class="container">
    <form @submit.prevent="addCard" class="form">
      <label for="name">
        <span>Название:</span>
        <input type="text" name="name" id="name" v-model="newCard.title" />
      </label>
      <label for="description">
        <span>Описание:</span>
        <input type="text" name="description" id="description" v-model="newCard.description" />
      </label>
      <button class="btn" type="submit">Добавить</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const newCard = ref({
  id: 0,
  title: '',
  description: '',
  completed: false,
})

const addCard = () => {
  console.log(newCard.value)
}

</script>

<style scope></style>
