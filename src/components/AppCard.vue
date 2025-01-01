<template>
  <div class="container">
    <h1 class="title">Wish List</h1>
    <div class="wrapper">
      <div class="card">
        <div class="card__title">{{ card.title }}</div>
        <div class="card__description">{{ card.description }}</div>
        <div class="card__is-actived">
          <div :class="{ 'card__is-active': card.isDone, 'card__is-not-active': !card.isDone }">
            {{ card.isDone ? 'Исполнено' : 'Не исполнено' }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
    index: {
        type: Number
    },
    card: {
        type: Object
    },
})

props.index
</script>

<style scope></style>
