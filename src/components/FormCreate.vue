<template>
  <div class="container">
    <h2 class="title-form">Форма заполнения</h2>
    <form action="" class="form">
        <label for="name">
            <span>Название:</span>
            <input type="text" name="name" id="name" :value="newCard.title" @input="setTitle">
        </label>
        <label for="description">
            <span>Описание:</span>
            <input type="text" name="description" id="description" :value="newCard.description" 
            @input="setDescription">
        </label>
        <button class="btn" type="submit">Добавить</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const newCard = ref({
  id: 0,
  title: '',
  description: '',
  completed: false,
})

const setTitle = (event) => {
  const value = event.target.value;
  newCard.value.title = value;
}

const setDescription = (event) => {
  const value = event.target.value;
  newCard.value.description = value;
}
</script>

<style scope>

</style>