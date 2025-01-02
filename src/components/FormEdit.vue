<template>
  <h2 class="title-form">Форма редактирования</h2>
  <div class="container">
    <form @submit.prevent="saveCard" class="form">
      <label for="name">
        <span>Название:</span>
        <input type="text" name="name" id="name" v-model="cards.title" />
      </label>
      <label for="description">
        <span>Описание:</span>
        <input type="text" name="description" id="description" v-model="cards.description" />
      </label>
      <button class="btn" type="submit">Сохранить</button>
    </form>
  </div>
</template>

<script setup>
const props = defineProps({
  card: {
    type: Object,
  },
})

const emit = defineEmits(['set-card', 'save-card'])

const setTitle = (event) => {
  const data = Object.assign({}, props.card)
  data.title = event.target.value
  emit('set-card', data)
}

const setDescription = (event) => {
  const data = Object.assign({}, props.card)
  data.description = event.target.value
  emit('save-card')
}

const saveCard = () => {
  emit('save-card', card.value)
}
</script>

<style scope></style>
