<template>
  <div class="container">
    <div class="wrapper">
      <WishList :cards="cards" @click-by-card="openCardForEdit" />
    </div>
    <FormEdit :card="cardForEdit" @set-card="updateCard" @save-card="saveCard" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import FormEdit from './components/FormCreate.vue'
import WishList from './components/WishList.vue'

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
])

const cardForEdit = ref({
  id: 0,
  title: '',
  description: '',
  completed: false,
})

const saveCard = () => {
  const newCard = Object.assign({}, cardForEdit.value)
  cards.value = cards.value.map((el) => (el.id === newCard.id ? newCard : el))
}

const updateCard = (card) => {
  cardForEdit.value = card
}

const openCardForEdit = (card) => {
  cardForEdit.value = Object.assign({}, card)
}
</script>

<style scope>
@import './assets/global.css';
@import './assets/card.css';
@import './assets/form.css';
</style>
